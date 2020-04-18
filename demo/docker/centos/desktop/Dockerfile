FROM centos:7
ENV container docker

# clean
RUN (cd /lib/systemd/system/sysinit.target.wants/; for i in *; do [ $i == \
systemd-tmpfiles-setup.service ] || rm -f $i; done); \
rm -f /lib/systemd/system/multi-user.target.wants/*;\
rm -f /etc/systemd/system/*.wants/*;\
rm -f /lib/systemd/system/local-fs.target.wants/*; \
rm -f /lib/systemd/system/sockets.target.wants/*udev*; \
rm -f /lib/systemd/system/sockets.target.wants/*initctl*; \
rm -f /lib/systemd/system/basic.target.wants/*;\
rm -f /lib/systemd/system/anaconda.target.wants/*;

#
RUN \
## systemd
yum -y install httpd; \
systemctl enable httpd.service; \
## desktop
yum -y groupinstall "GNOME Desktop"; \
## vnc
yum -y install tigervnc-server; \
## iptables
yum -y install iptables iptables-services; \
yum clean all;

#
VOLUME [ "/sys/fs/cgroup" ]

#
EXPOSE 80

#
CMD ["/usr/sbin/init"]

### docker build --rm -t local/c7-desktop .
