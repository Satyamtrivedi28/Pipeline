pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }

    }
    post {
         always {
             echo 'This will always run'
         }
         success {
             echo 'This will run only if successful'
             archiveArtifacts artifacts: '**/*.war', fingerprint: true
         }
        }
    }
}
