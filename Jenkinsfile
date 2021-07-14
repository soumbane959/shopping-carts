pipeline
{
    agent any
// uncomment the following lines by removing /* and */ to enable
    tools{
       maven 'maven' 
    }
    
    stages{
        stage('build'){
            steps{
                echo 'this is the MAVEN BUILD job'
                sh 'mvn compile'
            }
        }
        stage('test'){
            steps{
                echo 'this is the MAVEN TEST job'
                sh 'mvn test'
            }
        }
        stage('package'){
            steps{
                echo 'this is the MAVEN PACKAGE job'
                sh 'mvn package'
            }
        }

        stage('archive'){
            steps{
                echo 'this is the ARCHIVE job'
                archiveArtifacts '**/target/*.jar'
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
