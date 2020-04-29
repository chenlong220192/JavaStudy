FROM centos:7
ENV container docker

RUN \
yum -y install net-tools telnet passwd openssh*; \
yum clean all; \
echo chenlong | passwd --stdin root; \
ssh-keygen -q -t rsa -b 2048 -f /etc/ssh/ssh_host_rsa_key -N ''; \
ssh-keygen -q -t ecdsa -f /etc/ssh/ssh_host_ecdsa_key -N ''; \
ssh-keygen -t dsa -f /etc/ssh/ssh_host_ed25519_key -N '';

CMD ["/usr/sbin/sshd","-D"]

# docker build --rm -t local/centos7-ssh .
