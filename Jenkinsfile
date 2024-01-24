pipeline{

    agent any

    stages{

        stage('sonar quality status'){

            agent{

                docker{

                    image 'maven'
                }
            }
            steps{

              script{ 
                
                withSonarQubeEnv(credentialsId: 'sonar-token') {
                    sh 'sudo -i'
                    sh 'sudo apt-get install git'

                 sh 'mvn clean package sonar:sonar'

                 
                      }

                  }
            }  
        }
    }
}

    

          
