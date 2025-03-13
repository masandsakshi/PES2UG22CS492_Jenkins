pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/masandsakshi/PES2UG22CS492_Jenkins.git'
            }
        }
        
        stage('Check Files') {
            steps {
                script {
                    sh 'ls -la'  // Debugging step to check files in workspace
                }
            }
        }
        
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES2UG22CS492-1 main/hello.cpp' // Compile the C++ file
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
