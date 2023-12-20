pipeline
{
    agent any
    stages
    {
        stage('ContinuousDownload')
        {
            steps
            {
                git 'https://github.com/kisshk/multibranch.git'
            }
        }
        stage('ContinuousBuild')
        {
            steps
            {
                sh 'mvn package'
            }
        }
        stage('ContinuousDeployment')
        {
            steps
            {
                deploy adapters: [tomcat9(credentialsId: '8cc7d40a-bab0-438d-8dc2-f0d886815228', path: '', url: '172.31.82.247:8080')], contextPath: 'test1', war: '**/*.war'
            }
        }
        stage('ContinuousTesting')
        {
            steps
            {
                git 'https://github.com/intelliqittrainings/FunctionalTesting.git'
                sh 'java -jar /home/ubuntu/.jenkins/workspace/DeclarativePipeline/testing.jar'
            }
        }
       
        
        
    }
}























































     
       
       
        


