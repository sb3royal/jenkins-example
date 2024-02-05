pipeline {
    agent any

    environment {
        // Set JAVA_HOME to Java 17 installation path
        JAVA_HOME = '/path/to/java/17'
        PATH = "${JAVA_HOME}/bin:${env.PATH}"
    }

    stages {
        stage('Build') {
            steps {
                script {
                    // Use the withMaven step here
                    withMaven(maven: 'MavenInstallationName') {
                        sh 'mvn clean install'
                    }
                }
            }
        }
    }

    stages {
        stage('Compile Stage') {
            steps {
                script {
                    // Use Java 17 and Maven 3.8.4 (or the version you have installed)
                    withMaven(maven: 'maven_3_8_4', jdk: 'Java17') {
                        sh 'mvn clean compile'
                    }
                }
            }
        }

        stage('Testing Stage') {
            steps {
                script {
                    // Use Java 17 and Maven 3.8.4 (or the version you have installed)
                    withMaven(maven: 'maven_3_8_4', jdk: 'Java17') {
                        sh 'mvn test'
                    }
                }
            }
        }

        stage('Deployment Stage') {
            steps {
                script {
                    // Use Java 17 and Maven 3.8.4 (or the version you have installed)
                    withMaven(maven: 'maven_3_8_4', jdk: 'Java17') {
                        sh 'mvn deploy'
                    }
                }
            }
        }
    }
}
