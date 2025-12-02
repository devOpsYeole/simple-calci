pipeline {
    agent any
    tools {
        maven 'Maven-3.9.11'
    }

    stages {
        stage('Welcome Stage') {
            steps {
                echo "Welcome to Pipeline"
            }
        }

        stage('Maven Test') {
            steps {
                script {
                    if (isUnix()) {
                        // On Unix/Linux environments run shell
                        sh 'mvn -B test'
                    } else {
                        // On Windows environments run batch
                        bat 'mvn -B test'
                    }
                }
            }
        }

        stage('Maven Build') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'mvn -B -DskipTests=false install'
                    } else {
                        bat 'mvn -B -DskipTests=false install'
                    }
                }
            }
        }

        stage('Build Success') {
            steps {
                echo "Build Successful"
            }
        }

        stage('Final Success') {
            steps {
                echo "Final Successful"
            }
        }

        stage('Demo Success') {
            steps {
                echo "Demo Successful"
            }
        }
    }

    post {
        always {
            echo "Pipeline finished with status: ${currentBuild.currentResult}"
        }
    }
}
