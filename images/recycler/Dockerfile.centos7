#
# This is the default OpenShift Origin persistent volume recycler image.
#
# The standard name for this image is openshift/origin-recycler
#
FROM centos:centos7

RUN curl -o /etc/yum.repos.d/CentOS-OpenShift-Origin.repo https://tdawson.fedorapeople.org/centos/CentOS-OpenShift-Origin.repo

RUN INSTALL_PKGS="origin-recycle" && \
    yum install -y $INSTALL_PKGS && \
    rpm -V $INSTALL_PKGS && \
    yum clean all

ENTRYPOINT ["/usr/bin/recycle"]
