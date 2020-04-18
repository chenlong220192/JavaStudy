FROM local/c7-systemd
RUN yum -y install httpd; yum clean all; systemctl enable httpd.service
EXPOSE 80
CMD ["/usr/sbin/init"]

# docker build --rm -t local/c7-systemd-httpd .
