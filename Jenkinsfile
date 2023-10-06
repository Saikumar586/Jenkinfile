pipeline{

    agent { node { label 'AGENT-1' } }

    options{

        timeout(time: 1 , unit: 'SECONDS')
    }

    stages{

        stage('Build'){
            steps{
                

                 echo"Build stage"

                
            }
        }
    
        stage('test'){
            steps{
                

                 echo"Build test"

                
            }
        }
    
        stage('deploye'){
            steps{
                

                 echo"Build deploye"

                
            }
        }
    post {

        success{

            echo "when build success"
            
        }
    }
    post {
        failure{
            
            echo "when build failure"
        }
    }

    }
}