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
                bat 'mvn test'
            }
        }      

        stage('Maven Build') {
            steps {
                bat 'mvn install'
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
                echo "Final Successful"
            }
        }    

    }
}
