FROM ubuntu:latest

RUN apt-get update
RUN apt-get install -y gnupg
RUN apt-get install -y ca-certificates

RUN echo "deb [arch=amd64] https://pkg.osquery.io/deb deb main" | tee /etc/apt/sources.list.d/osquery.list
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 1484120AC4E9F8A1A577AEEE97A80C63C9D8B80B \
    && apt-get update \
    && apt-get install -y osquery
RUN apt-get install -y python3

