pipeline{

    agent { node { label 'AGENT-1' } }

    options{

        timeout(time: 1 , unit: 'SECONDS')
    }

    stages{

        stage('Build')
        {
            steps{
                

                 echo"Build stage"

                
            }
        }
    
        stage('test')
        {
            steps{
                

                 echo"Build test"

                
            }
        }
    
        stage('deploye')
        {
            steps{
                

                 echo "Build deploye"
                 4512

                
            }
        }
    }

    post { 
        always { 
            echo 'I will always run whether job is success or not'
        }
        success{
            echo 'I will run only when job is success'
        }
        failure{
            echo 'I will run when failure'
    }
    
        
    }
     
    
    


}
