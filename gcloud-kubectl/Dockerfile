FROM google/cloud-sdk:alpine

RUN curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.15.1/bin/linux/amd64/kubectl \
    && chmod u+x kubectl && mv kubectl /bin/kubectl

ADD datnt-service-account.json /root/.config/
ADD README.md /root/
WORKDIR /root/

RUN apk add alpine-sdk gettext
ADD get_helm.sh /get_helm.sh
RUN chmod +x /get_helm.sh
RUN /get_helm.sh