# Setup Docker VM + Container (for pre-existing projects with docker file already):

##### 1. Make sure you have [Docker toolbox](https://docs.docker.com/mac/step_one/) installed.

##### 2. Open Docker Quickstart Terminal in launchpad!

##### 3. Build the container:
  - `$ docker-compose up` (or `$ docker-compose build` first if that barfs)
  - More info: [docker-compose up](https://docs.docker.com/compose/reference/up/)

  > Should only have to do this whenever starting up the VM or dockerfile has changed.

#### 4. Probably will have to set the docker port and host port to be the same so can boot up and access it locally:
  - Open VirtualBox
  - Open `Settings`
  - Open `Network`
  - Open `Port Forwarding`
  - Click `Add` icon
  - name: `rails` (or `middleman` or whatevs), host port: `3000`, guest port: `3000`
  - Open `localhost:3000` (or whatever port # you set it to) in browser, should see the app working now!

#### 5. If not working, restart your VM by trying:
  - `$ docker-machine restart default`
  - `$ eval $(docker-machine env default)`

#### 6. Issues with default virtual machine?
  - Open VirtualBox
  - Turn off the "default" machine
  - Run Docker Quickstart again!

#### 7. Other Tips:
  - You can build & run 2 containers at the same time on the same VM.  ...But they have to have different port numbers!
  - To run `rails console`: ```$ docker-compose run web rails console```
