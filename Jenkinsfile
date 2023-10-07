pipeline{

    agent { node { label 'AGENT-1' } }

    options{

        timeout(time: 59 , unit: 'SECONDS')
       //retry(2)
        //parallelsAlwaysFailFast() 
        
    }

    environment {

        username = 'Saikumar'
    }

    //triggers{ cron('*/5 * * * *') }


    //   parameters {
    //     string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

    //     text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

    //     booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

    //     choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

    //     password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    // }

    stages{

        stage('Build')
        {
            steps{
                

                 echo "Build stage"

                 sh '''
                 ls -l
                pwd
                echo "hello git hub web hook checking "
                printenv
                

                '''
                
            }
        }
      
      stage('params') {
            steps {
                echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"
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
                // error 'if failure'

                
            }
        }
        stage('Parallel Stage') {
 
            parallel {
                stage('Branch A') {
                    steps {
                        echo "On Branch A"
                        sh 'sleep 10'
                    }
                }
                stage('Branch B') {
                    steps {
                        echo "On Branch B"
                        sh 'sleep 10'
                    }
                }
                stage('Branch C') {
                    stages {
                        stage('Nested 1') {
                            steps {
                                echo "In stage Nested 1 within Branch C"
                                sh 'sleep 10'
                            }
                        }
                        stage('Nested 2') {
                            steps {
                                echo "In stage Nested 2 within Branch C"
                                sh 'sleep 10'
                            }
                        }
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
    }
}
