FROM centos:latest
LABEL maintainer="matt.howe"

#RUN yum check-update
RUN yum update -y

#Prevent Login to Accounts With Empty Password
RUN echo 'root:password123!@#' | chpasswd
RUN sed --follow-symlinks -i 's/\<nullok\>//g' /etc/pam.d/system-auth
RUN sed --follow-symlinks -i 's/\<nullok\>//g' /etc/pam.d/password-auth

#TEST ONLY FOR SCANNING, REMOVE
#ENTRYPOINT ["/bin/bash"]
