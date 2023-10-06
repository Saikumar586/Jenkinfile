pipeline{

    agent { node { label 'AGENT-1' } }

    options{

        timeout(time: 1 , unit: 'SECONDS')
       retry(2)
        parallelsAlwaysFailFast() 
    }

      parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    stages{

        stage('Build')
        {
            steps{
                

                 echo "Build stage"

                 sh '''
                 ls -l
                pwd
                echo "hello"
                

                '''
                
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
                 error 'if failure'

                
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
