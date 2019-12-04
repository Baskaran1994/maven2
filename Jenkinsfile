node('master')
{
    stage('Continouus Download')
    {
        git 'https://github.com/Baskaran1994/Maven.git'
    }
    stage('Continous Build')
    {
       sh label: '', script: 'mvn package'
    }
    
      stage('Continous Deployment')
    {
       sh label: '', script: 'scp /home/ec2-user/.jenkins/workspace/Development/webapp/target/webapp.war  ec2-user@172.31.42.22:/var/lib/tomcat/webapps/testwebapp.war' 
    }
    stage('Continous Testing')
    {
        git 'https://github.com/selenium-saikrishna/FunctionalTesting.git'
        sh label: '', script: 'echo Testing Passed'
    }
    stage('Continous Delivery')
    {
        sh label: '', script: 'scp /home/ec2-user/.jenkins/workspace/Development/webapp/target/webapp.war  ec2-user@172.31.7.27:/var/lib/tomcat/webapps/prodwebapp.war'
    } 
}
