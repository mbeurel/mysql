FROM mysql:5.7
ARG USER_ID
ARG GROUP_ID

RUN userdel -f mysql &&\
    if getent group mysql ; then groupdel mysql; fi &&\
    groupadd -g ${GROUP_ID} mysql &&\
    useradd -l -u ${USER_ID} -g mysql -G sudo mysql -s /bin/bash &&\
    install -d -m 0755 -o mysql -g mysql /var/lib/mysql


