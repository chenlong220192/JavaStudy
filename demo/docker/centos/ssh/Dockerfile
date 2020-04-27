FROM local/centos7-clean

RUN yum -y install net-tools passwd openssh*
RUN yum clean all
RUN echo chenlong | passwd --stdin root
RUN ssh-keygen -q -t rsa -b 2048 -f /etc/ssh/ssh_host_rsa_key -N ''
RUN ssh-keygen -q -t ecdsa -f /etc/ssh/ssh_host_ecdsa_key -N ''
RUN ssh-keygen -t dsa -f /etc/ssh/ssh_host_ed25519_key -N ''

CMD ["/usr/sbin/sshd","-D","&"]

# docker build --rm -t local/centos7-ssh .
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
!!!!!!!!!!!!!!! 生成镜像启动不了，尚未解决!!!!!!!
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
