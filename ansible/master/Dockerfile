# MASTER image - used to create the master container to manage hosts

FROM ansible_base:latest

RUN apt-get update \
    && apt-get install --no-install-recommends --no-install-suggests -y \
    ansible

COPY ansible /var/ans/

WORKDIR /var/ans

RUN ssh-keygen -t rsa -N 12345 -C "master key" -f master_key
