pipeline
{
    agent any 
    stages
    {
        
       
         stage ('building the code using maven')
        {
            steps
            {
            withMaven (maven : 'maven_3_5_3')
            {
                 sh 'mvn install'
            }
            }
            
        }
        stage ('deploy the code ')
        {
            steps
            {
                sh ' cp 	-R /var/lib/jenkins/workspace/Development_Project/target/* /opt/apache-tomcat-8.0.11/webapps/ '
            }
            
        }
    }
}
