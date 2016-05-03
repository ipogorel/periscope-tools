tools
=====

Tools and utility functions used to build and develop Periscope libraries.

## To create a dev environment:

1. Create an periscope directory to hold all of the projects.

  ```shell
  mkdir periscope
  ```
2. Change to the new directory

  ```shell
  cd periscope
  ```
3. Clone this repository into the `tools` directory.  This repo contains the helper tools for creating the dev environment.

  ```shell
  git clone https://github.com/privosoft/periscope-tools.git
  ```
4. Clone the periscope-demo-app also which is the base app for testing -

  ```shell
  git clone https://github.com/privosoft/periscope-demo-app.git
  ```
5. Change directory into periscope-demo-app

  ```shell
  cd periscope-demo-app

 ```
6. Install the periscope-demo-app application's dependencies:

  ```shell
  npm install
  jspm install
  ```
7. Build the dev environment.  This will create all of the directories inside of `periscope` under the proper name, `git clone` them all and then perform a `gulp build`. If the directories were created previously `build-dev-env` command will just rebuild them.

  ```shell
  gulp build-dev-env
  ```
Alternatively, run `gulp pull-dev-env` to only pull down each `periscope` dependency and not perform builds.


8. Now you have the ability to update the repos locally, make changes, and use those in the periscope-demo-app in the `periscope` directory by using the `gulp update-own-deps` command.
Note: before run `update-own-deps` command please make sure that the changed repos were properly built othervise run `build-dev-env` one more time.



