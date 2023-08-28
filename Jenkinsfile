pipeline{
    
    tools{
        maven 'mymaven'
    }
    agent any
    stages{
        stage('clonerepo')
        {
            steps{
                git 'https://github.com/Pravi296/DevOpsCodeDemo.git'
            }
        }
        stage('compile')
        {
            steps{
                sh 'mvn compile'
            }
        }
        stage('Code Review')
        {
            steps{
                sh 'mvn pmd:pmd'
            }
            
        }
        stage("Test the code")
        {
            steps{
                sh 'mvn test'
            }
        }
        stage('Package code')
        {
            steps{
                sh 'mvn package'
            }
        }
    }
    

    
    
}
