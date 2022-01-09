pipeline{
    agent any
    stages{
        stage('build application'){
            steps{
               sh 'mvn clean package'
            }
            post{
                success{
                    echo 'Now Archiving ...'
                    archiveArtifacts artifacts : '**/*.war'
                }
            }
        }
    }
}