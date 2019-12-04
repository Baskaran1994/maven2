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
    
    
}
