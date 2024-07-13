# emptyhammock-role-docker-application

This is an Ansible role that, in conjunction with a number of other Emptyhammock
roles, handles provisioning and deployment of Django applications which run
in Docker containers.

It is oriented closely to Emptyhammock projects, but you may find some useful
snippets here.

## Ansible variables

| Variable                    | Value                                                               | Default                                            |
|-----------------------------|---------------------------------------------------------------------|----------------------------------------------------|
| `aws_account_id`            | AWS account id, used in default `image_registry_url`                | none                                               |
| `aws_region`                | AWS region                                                          | `us-east-1`                                        |
| `AWS_ECR_ACCESS_KEY_ID`     | AWS access key id for pulling image from ECR                        | none                                               |
| `AWS_ECR_SECRET_ACCESS_KEY` | AWS access key for pulling image from ECR                           | none                                               |
| `cert_source`               | `manual`, `self-signed`, `certbot`                                  | `self-signed`                                      |
| `certbot_dir`               | directory managed by certbot                                        | none                                               |
| `certificate_domains`       | list of domains for SSL certificate                                 | `canonical_server_name` with and without `www.`    |
| `docker_env`                | dictionary of environment variables passed to Docker container      | none                                               |
| `docker_volumes`            | list of Docker volume parameters                                    | `static_dir` and `media_dir` are mirrors with host |
| `image_registry_url`        | ECR URL for project's Docker image                                  | `project_name` repo within AWS account and region  |
| `media_dir`                 | directory within `project_dir` for media files served by webserver  | none                                               |
| `project_dir`               | directory within `project_user`'s HOME for project files            | none                                               |
| `project_name`              | name of project, used in default `image_regitry_url`                | none                                               |
| `project_user`              | Linux user which owns project                                       | none                                               |
| `script_dir`                | directory within `project_dir` for management scripts               | none                                               |
| `static_dir`                | directory within `project_dir` for static files served by webserver | none                                               |
