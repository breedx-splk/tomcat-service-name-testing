# tomcat-service-name-testing

Can we detect the service name in tomcat?

```
./gradlew war
export TH=<ip of your host>
export THU=<remote user>
rsync -avv --progress splunk-otel-javaagent-1.32.1.jar $THU@$TH:~
rsync -avv --progress $THU@$TH:~
ssh $THU@$TH
sudo apt install -y unzip zip
curl -s "https://get.sdkman.io" | bash
sdk install java 21.0.3-tem
https://dlcdn.apache.org/tomcat/tomcat-10/v10.1.24/bin/apache-tomcat-10.1.24.zip
unzip apache-tomcat-10.1.24.zip
mv tomcat-service-name-testing.war apache-tomcat-10.1.24/webapps/
cd apache-tomcat-10.1.24
vim bin/catalina.sh
<insert CATALINA_OPTS="-javaagent:/home/<user>/splunk-otel-javaagent-1.32.1.jar"
curl -sSL https://dl.signalfx.com/splunk-otel-collector.sh > /tmp/splunk-otel-collector.sh && \
  sudo sh /tmp/splunk-otel-collector.sh --with-instrumentation --realm us0 
  --deployment-environment tctest -- "<your ingest token>"
sh bin/catalina.sh start
curl http://${TH}:8080/tomcat-service-name-testing/rawr
```