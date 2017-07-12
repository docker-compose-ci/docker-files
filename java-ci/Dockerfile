FROM java

RUN apt-get update && \
apt-get install wget unzip -y && \
cd ~ && \
wget https://github.com/spotbugs/spotbugs/archive/3.1.0_RC3.zip && \
unzip 3.1.0_RC3.zip && \
echo "PATH=$PATH:~/spotbugs-3.1.0-RC3/bin" >> ~/.bashrc

