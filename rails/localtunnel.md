## How to Use localtunnel to share your local dev machine and test stuff you might need to be able to call back your local machine:

##### Install localtunnel:
  - Install the package globally: ```$ npm install -g localtunnel```
  - Start a webserver: ```lt --port 8000```
  - More info: [LocalTunnel](https://localtunnel.me/)

##### Special info for using localtunnel with pow:
  - Add localtunnel.me as a external domain for pow
    - ```$ echo "export POW_EXT_DOMAINS=localtunnel.me" > ~/.powconfig```
  - Kill the pow process
    - ```$ killall pow```
  - Open a tunnel with a subdomain matching your pow subdomain:
    - ```$lt --port 80 --subdomain mygreatapp```
  - Visit `https://mygreatapp.localtunnel.me`
  - More info: [Using localtunnel with pow](https://github.com/localtunnel/localtunnel/wiki/Using-localtunnel-with-pow)
