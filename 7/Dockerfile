FROM centos:latest
MAINTAINER yujmo yujmo94@gmail.com
RUN rm -rf /etc/yum.repos.d/CentOS-[DSfCMV]* \
    && yum install epel-release -y && yum clean all && yum update -y && yum install nginx supervisor -y \
    && rm -rf /etc/nginx/nginx.conf 

COPY nginx.conf /etc/nginx/nginx.conf
COPY index.html /opt/sftp/web/upload/index.html
COPY supervisord.conf /etc/supervisord.conf
EXPOSE 80 
CMD ["/usr/bin/supervisord"]
