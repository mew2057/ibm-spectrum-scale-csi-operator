FROM quay.io/operator-framework/ansible-operator:v0.11.0
MAINTAINER jdunham@us.ibm.com

LABEL name="IBM Spectrum Scale CSI Operator" \
      vendor="ibm" \
      version="1.0" \
      release="1" \
      run='docker run ibm-spectrum-scale-csi-operator' \
      summary="An Ansible based operator to run and manage the deployment of the IBM Spectrum Scale CSI Driver." \
      description="An Ansible based operator to run and manage the deployment of the IBM Spectrum Scale CSI Driver." 

#
#RUN REPOLIST=ubi-7,ubi-7-optional \
#    yum -y update-minimal --disablerepo "*" --enablerepo ubi-7 --disableplugin=subscription-manager --setopt=tsflags=nodocs \
#      --security --sec-severity=Important --sec-severity=Critical && \
#    yum -y install --disablerepo "*" --enablerepo ${REPOLIST} --disableplugin=subscription-manager --setopt=tsflags=nodocs ${INSTALL_PKGS} && \
#    yum clean all

COPY licenses /licenses
COPY watches.yaml ${HOME}/watches.yaml
COPY build/_output/bin/ibm-spectrum-scale-csi-operator ${OPERATOR}
COPY roles/ ${HOME}/roles/




