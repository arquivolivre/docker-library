FROM jenkins

USER root
RUN echo "deb http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main" >> /etc/apt/sources.list
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367
RUN apt-get update
RUN apt-get install -y ansible
RUN apt-get purge -y python-pip
RUN wget https://bootstrap.pypa.io/get-pip.py
RUN python ./get-pip.py
RUN apt-get install -y gcc python-dev libffi-dev libssl-dev python-pip
RUN pip install ara pymysql
COPY ansible.cfg /etc/ansible
USER jenkins
