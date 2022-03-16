pipeline{
    agent any
    tools{
        maven 'maven-3.8.5'
    }
    stages{
        stage('check-out git'){
            steps{
                git 'https://github.com/prabhat-dsc/hello-world-war.git'
            }
        }
        stage('Build-job'){
            steps{
                sh 'mvn clean install'
            }
        }
        stage('deploy-tomcat'){
            steps{
                sh 'sudo su - test -c "ansible-playbook hello-world.yml"'
            }
        }
    }
}
