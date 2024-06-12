# tomcat-service-name-testing

Can we detect the service name in tomcat?

```
./gradlew war
export TH=<ip of your host>
export THU=<remote user>
rsync -avv --progress $THU@$TH:~
ssh $THU@$TH
curl -s "https://get.sdkman.io" | bash
sdk install java 21.0.3-tem
https://dlcdn.apache.org/tomcat/tomcat-10/v10.1.24/bin/apache-tomcat-10.1.24.zip
unzip apache-tomcat-10.1.24.zip
```