# Debugging random test failures and dependencies.

#### Problem:
- If I ran our test suite randomized (`bin/rspec --order rand` or `--order rand` in the `.rspec` file), I would get failing specs due to `I18n.locale` being set and not cleared in the specs.

#### Debug Process:
- Run tests randomized: `bin/rspec --order rand`
- Run tests with a seed specified from the randomized test above PLUS with `--bisect` option: `bin/rspec --seed <SEED NUMBER> --bisect`
- This will take a while depending on # of tests... (~1400 took ~30 min)
- RSpec finds the minimal set of examples (probably 2) that reproduce the failure.
- Debug and fix the issue.
- For this case, I need to make sure the I18n.default_locale was set after each test, since for some specs, we would set a `:nl` or `:fr` locale.  I fixed it by adding `config.after(:each) { I18n.locale = I18n.default_locale }` to my `rails_helper.rb` file.  I also left my tests randomized now, by adding `--order rand` to the `.rspec` file.

#### References:
- [I18n.locale is a global object, so when it's changed in a spec, it persists](https://github.com/svenfuchs/i18n/issues/256)
- [Using RSpec Bisect](https://relishapp.com/rspec/rspec-core/docs/command-line/bisect)
- [Specs of my Rails app fail randomly because of wrong default locale](http://stackoverflow.com/questions/36040661/specs-of-my-rails-app-fail-randomly-because-of-wrong-default-locale)
