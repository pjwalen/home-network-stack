FROM ubuntu:bionic
USER root
CMD dhcpd -user dhcpd -group dhcpd -f -d -4 -pf /run/dhcp-server/dhcpd.pid -cf /etc/dhcp/dhcpd.conf
EXPOSE 67:67/udp
RUN apt-get update; \
    apt-get install -y isc-dhcp-server; \
    touch /var/lib/dhcp/dhcpd.leases; \
    chown root:dhcpd /var/lib/dhcp /var/lib/dhcp/dhcpd.leases; \
    chmod 775 /var/lib/dhcp; \
    chmod 664 /var/lib/dhcp/dhcpd.leases; \
    mkdir /run/dhcp-server;