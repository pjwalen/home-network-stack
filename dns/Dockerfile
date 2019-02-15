FROM ubuntu:bionic
USER root
RUN apt-get update; apt-get install -y bind9; mkdir /run/named; chmod 775 /run/named;  chown root:bind /run/named; apt-get clean;
CMD /usr/sbin/named -g -u bind
EXPOSE 53:5352
EXPOSE 53:5352/udp
