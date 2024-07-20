# Changes and migration requirements

## Version 0.0.7

* Install manage.sh script so that remote-manage scripts can work.

## Version 0.0.6

* Fix emptyhammock-maintenance's failure to parse the output of pip_freeze.sh.

## Version 0.0.5

* For the collectstatic step only, revert the change to run the container as the
  project user/group.

## Version 0.0.4

* Run the Docker container as the project user/group.

## Version 0.0.3

* Add default values for `docker_volumes`, `aws_region`, and `image_registry_url`.
* Add documentation of optional and required Ansible variable settings.

## Version 0.0.2

* Create project directory (e.g., /home/MYPROJECT/MYPROJECT) with 0755 permissions so
  that the web server can serve static files from a subdirectory therein.

## Version 0.0.1

* initial version
