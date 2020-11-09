pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
         success {  
             echo 'This will run only if successful'
	     archiveArtifacts artifacts: '**/*.war', fingerprint: true
         }  
        }
    }
}
