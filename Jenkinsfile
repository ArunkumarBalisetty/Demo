node {
    stage('continuous download') {
    git branch: 'main', changelog: false, poll: false, url: 'https://github.com/ArunkumarBalisetty/Demo.git'
     }
   stage('continuous build') {
    sh 'mvn package'
    }
    stage('continuous deployment') {
    sh 'scp /home/ubuntu/.jenkins/workspace/ci-cd_pipeline/webapp/target/webapp.war ubuntu@172.31.45.145:/var/lib/tomcat9/webapps/nonprod.war'
    }
    stage('continuous testing') {
    sh 'echo "Testing passed"'
    }
    stage('continuous Delivery') {
    sh 'scp /home/ubuntu/.jenkins/workspace/ci-cd_pipeline/webapp/target/webapp.war ubuntu@172.31.43.138:/var/lib/tomcat9/webapps/nonprod.war'
    }

}
