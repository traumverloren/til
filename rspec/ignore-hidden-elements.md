# Testing Hidden Elements, aka I Need to test a modal (hidden element) with Rspec/Capybara

To confirm that a modal partial in the view (like below)

    ```
      - if @unverified_thing

        = render partial: "modal_verify_account"

        - content_for :javascript do
          :javascript
            $(function(){
              $('#modal-verify-thing').modal('show')
            });
    ```

is accessible to testing, in your spec, you gotta let Capybara know to not ignore hidden elements:

    ```  
        before do
          Capybara.ignore_hidden_elements = false
        end

        after do
          Capybara.ignore_hidden_elements = true
        end
    ```
