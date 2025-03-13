pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o YOUR_SRN-1 main.cpp' // Compile the C++ file
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './YOUR_SRN-1' // Run the compiled C++ file and print output
                }
            }
        }
        
        stage('Deploy') {
            steps {
                script {
                    sh 'echo "Deploying application..."'
                }
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
