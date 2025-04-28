pipeline {
    agent any
    tools {
        maven 'M3'  // The Maven version you configured
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/SagarPradhan85211/Bank-Application'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean install'  // Build the project
            }
        }
        stage('Run Application') {
            steps {
                bat 'mvn spring-boot:run'  // Run the new application java -jar target/bank-0.0.1-SNAPSHOT.war
            }
        }
    }
}
