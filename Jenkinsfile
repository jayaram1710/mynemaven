pipeline
{
    agent any
    stages
    {
        stage('ContinuousDownload_Master')
        {
            steps
            {
                git 'https://github.com/intelliqittrainings/maven.git'
            }
        }
        stage('ContinuousBuild_Master')
        {
            steps
            {
                sh 'mvn package'
            }
        }
        stage('ContinuousDeployment_Master')
        {
            steps
            {
                sh 'scp /home/ubuntu/.jenkins/workspace/test/webapp/target/webapp.war ubuntu@172.31.60.120:/var/lib/tomcat9/webapps/newtestapp.war'
            }
        }
    }
}
