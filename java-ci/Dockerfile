FROM java

RUN apt-get update && \
apt-get install wget unzip -y && \
cd ~ && \
wget http://repo.maven.apache.org/maven2/com/github/spotbugs/spotbugs/3.1.0-RC2/spotbugs-3.1.0-RC2.zip -O 3.1.0_RC2.zip&& \
unzip 3.1.0_RC2.zip && \
ln -s ~/spotbugs-3.1.0-RC2/bin/spotbugs /bin/spotbugs

RUN apt-get remove wget unzip -y && \
apt-get autoremove --purge -y

CMD /bin/spotbugs

