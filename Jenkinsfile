pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES2UG22CS492-1 hello.cpp' // Compile the C++ file
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS492-1' // Run the compiled C++ file and print output
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
