pipeline
{
    agent any
    stages {
        stage('download') {
             steps {
            git branch: 'main', changelog: false, poll: false, url: 'https://github.com/ArunkumarBalisetty/Demo.git'
                   }
            }

        stage('build') {
               steps {
            sh 'mvn package'
                   }
            }

    }

}
