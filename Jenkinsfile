pipeline {
    agent { docker 'maven:3.3.3' }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
    post {
	success {
            echo 'Build successful!:)'
        }
        failure {
            echo 'Build failed!:('
        }
    }
}

