# testproj
# mvn 打包部署脚本
#!/bin/bash
git pull origin master;
cd testproj/webdemo;
mvn package;
cp target/webdemo.war ${tomcat_dir}/webapps;
${tomcat_dir}/bin/startup.sh
