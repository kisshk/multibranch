pipeline
{
    agent any
    stages
    {
        stage('ContDownload')
        {
            steps
            {
                script
                {
                    cicd.newDownload("maven.git")
                }
            }
        }
        stage('ContBuild')
        {
            steps
            {
                script
                {
                    cicd.newBuild()
                }
            }
        }
        stage('ContDeployment')
        {
            steps
            {
                script
                {
                    cicd.newDeploy("DeclarativePipelinewithSharedLibrarires","172.31.32.68","testapp")
                }
            }
        }
    }
}























































     
       
       
        


