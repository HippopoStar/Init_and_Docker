# https://gitlab.com/gitlab-org/gitlab-ce
# https://gitlab.com/gitlab-org/omnibus-gitlab/tree/master/docker
# https://docs.gitlab.com/omnibus/docker/
# https://about.gitlab.com/installation/

# login: root
# password: 5iveL!fe

# docker build --tag ex03 ./
# docker run -d --name ex03 --hostname gitlab.ex03.com -p 443:443 -p 80:80 -p 22:22 --name ex03

FROM ubuntu:16.04

SHELL [ "/bin/sh" , "-c" ]

RUN apt-get update && apt-get -y install openssh-server ca-certificates curl
RUN curl -o /tmp/gitlab_install_script.deb.sh https://packages.gitlab.com/install/repositories/gitlab/gitlab-ee/script.deb.sh
RUN bash /tmp/gitlab_install_script.deb.sh
RUN EXTERNAL_URL="http://gitlab.ex03.com" apt-get install gitlab-ee

EXPOSE 443 80 22
