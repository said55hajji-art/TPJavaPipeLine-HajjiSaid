pipeline {
    agent any

    tools {
      
        maven 'Maven'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/said55hajji-art/TPJavaPipeLine-HajjiSaid.git'
            }
        }

        stage('Build') {
            steps {
                // 'clean package' compile le code et génère le fichier JAR/WAR
                sh 'mvn clean package -DskipTests'
            }
        }

        stage('Test') {
            steps {
                // Exécution des tests unitaires
                sh 'mvn test'
            }
        }
    }
}
