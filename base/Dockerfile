FROM centos:7

RUN yum install -y wget iproute && \
    wget -O install.sh https://download.bt.cn/install/install_6.0.sh && \
    echo "y" | sh install.sh && \
    echo "username" | bt 6 && \
    echo "password" | bt 5 && \
    rm -f /www/server/panel/data/admin_path.pl

EXPOSE 8888 80 443

CMD bt 3 && bt default && tail -f /dev/null
