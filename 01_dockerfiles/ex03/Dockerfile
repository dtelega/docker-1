FROM ubuntu:18.04
MAINTAINER dtelega <dtelega@student.unit.ua>

RUN apt-get update -q &&  apt-get install -yq curl ca-certificates openssh-server postfix wget apt-transport-https 

#install gitlab
RUN wget https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh && chmod 777 script.deb.sh && ./script.deb.sh
RUN apt-get install -y gitlab-ce

#sshd
RUN apt update && apt-get install -y tzdata && \
	apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

EXPOSE 443 80 22

ENTRYPOINT (/opt/gitlab/embedded/bin/runsvdir-start &) && gitlab-ctl reconfigure && tail -f /dev/null
