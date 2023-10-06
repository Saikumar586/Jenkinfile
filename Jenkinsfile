pipelines{

    agent any

    stages{

        stage('Build'){
            steps{
                
                ssh '''

                echo "Build stage"

                '''
            }
         stage('test'){
            steps{

                ssh '''

                echo "test stage"

                '''
            }
         }
         stage('deploye'){
            steps{

                ssh '''

                echo "Deploy"

                '''
            }
        }
    }


}
    }