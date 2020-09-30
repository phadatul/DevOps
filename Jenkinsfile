pipeline{
    agent any
    stages{
        stage("One"){
            steps{
                echo "========executing A========"
            }
         
        }
        stage("Two"){
            steps{
                input("Do you want to continue?")
            }
        }

        stage('Three'){
            when{
                not{
                    branch "master"
                }}
                steps{
                    echo "hello, three"
                }
            
        }
        stage('Four'){
            parallel{
                stage('Unit Test'){
                    steps{
echo "UNit test done"
                    }
                }

                stage('Integration test'){
                    steps{
echo "Integration test done"
                    }
                }
            }
        }
    }
}
   