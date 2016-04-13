#
# This is the base image from which all OpenShift Origin images inherit. Only packages
# common to all downstream images should be here.
#
# The standard name for this image is openshift/origin-base
#
FROM centos:centos7

RUN curl -o /etc/yum.repos.d/CentOS-OpenShift-Origin.repo https://tdawson.fedorapeople.org/centos/CentOS-OpenShift-Origin.repo

RUN INSTALL_PKGS="which git tar wget hostname sysvinit-tools util-linux bsdtar \
        socat ethtool device-mapper iptables e2fsprogs xfsprogs" && \
    yum install -y $INSTALL_PKGS && \
    rpm -V $INSTALL_PKGS && \
    yum clean all
