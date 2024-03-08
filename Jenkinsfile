pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Compile the .cpp file using shell script
                sh 'g++ -o PES1UG21CS104 hello.cpp'
            }
        }
        stage('Test') {
            steps {
                // Print output of .cpp file using shell script
                sh './PES1UG21CS104'
            }
        }
        stage('Deploy') {
            steps {
                // Placeholder for deployment steps
                echo 'Deploying...'
            }
        }
    }
    post {
        failure {
            // Display 'pipeline failed' in case of any errors within the pipeline
            echo 'Pipeline failed'
        }
    }
}
