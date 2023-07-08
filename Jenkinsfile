node('built-in') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/ArunkumarBalisetty/Demo.git'
	}
    stage('Continuous Build') 
	{
    sh 'mvn package'
	}
    stage('Continuous Deployment') 
	{
    sh 'scp /home/ubuntu/.jenkins/workspace/scpipeline/webapp/target/webapp.war   ubuntu@172.31.34.145:/var/lib/tomcat9/webapps/qaenv1.war'
	}
    stage('Continuous Testing') 
	{
              sh 'echo "Testing Passed please check the result"'
	}
    stage('Continuous Delivery') 
	{
           sh 'scp /home/ubuntu/.jenkins/workspace/scpipeline/webapp/target/webapp.war   ubuntu@172.31.22.88:/var/lib/tomcat9/webapps/prodenv.war'
	}
}
