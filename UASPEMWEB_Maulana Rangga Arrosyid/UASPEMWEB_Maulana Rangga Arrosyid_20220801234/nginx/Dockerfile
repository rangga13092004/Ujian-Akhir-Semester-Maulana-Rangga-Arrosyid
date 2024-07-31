FROM tianon/true

LABEL maintainer="Your Name <arrosyidtekniklistrikmaulanara@gmail.com>"

RUN apt-get update && \
    apt-get install -y wget && \
    wget https://www.apachefriends.org/xampp-files/7.4.9/xampp-linux-x64-7.4.9-0-installer.run && \
    chmod +x xampp-linux-x64-7.4.9-0-installer.run && \
    ./xampp-linux-x64-7.4.9-0-installer.run --mode unattended

COPY startup.sh /opt/lampp/startup.sh
RUN chmod +x /opt/lampp/startup.sh

EXPOSE 80 443 3306

CMD ["/opt/lampp/startup.sh"]
