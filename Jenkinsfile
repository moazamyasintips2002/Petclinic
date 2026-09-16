pipeline {
    agent any
    
    tools {
        jdk "jdk11"
        maven "maven3"
    }

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'feature2', url: 'https://github.com/jaiswaladi246/Petclinic.git'
            }
        }
        
        stage('Compile') {
            steps {
                sh "mvn clean compile"
            }
        }
        
        stage('Package') {
            steps {
                // Removed 'clean' so it reuses the compiled files
                sh "mvn package" 
            }
        }
      }
   }
}

