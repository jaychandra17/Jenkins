pipeline {
    agent any

    stages {
        stage('Compile Stage') {
            steps {
                // Using the specified Maven installation
                withMaven(maven: 'maven_3_9_6') {
                    sh '/Users/gowe/Downloads/apache-maven-3.9.6/bin/mvn clean compile'
                }
            }
        }

        stage('Testing Stage') {
            steps {
                // Using the specified Maven installation
                withMaven(maven: 'maven_3_9_6') {
                    sh '/Users/gowe/Downloads/apache-maven-3.9.6/bin/mvn test'
                }
            }
        }

        stage('Deployment Stage') {
            steps {
                // Using the specified Maven installation
                withMaven(maven: 'maven_3_9_6') {
                    sh '/Users/gowe/Downloads/apache-maven-3.9.6/bin/mvn deploy'
                }
            }
        }
    }
}
