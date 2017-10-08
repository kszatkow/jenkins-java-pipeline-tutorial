pipeline {

    agent { docker 'maven:3.3.3' }
    
    stages {
        stage('Build') {
            steps {
                sh 'mvn --version'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing'
            }
        }
        
	stage('Sanity check') {
            steps {
                input "Deploy?"
            }
        }	

        stage('Deploy') {
            steps {
                echo 'Deploying'
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

