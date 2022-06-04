pipeline{
    agent{
        label "node"
    }
    stages{
        stage("Checkout"){
            steps{
                script {
                    // The below will clone your repo and will be checked out to master branch by default.
                    git credentialsId: 'ff236995-e4d2-42fe-b47f-eb4110cab8d1', url: 'https://github.com/phamhaiddc/jenkins.git'
                    // Do a ls -lart to view all the files are cloned. It will be clonned. This is just for you to be sure about it.
                    sh "ls -lart ./*" 
                    // List all branches in your repo. 
                    sh "git branch -a"
                    // Checkout to a specific branch in your repo.
                    sh "git checkout dev"
                }
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========A executed successfully========"
                }
                failure{
                    echo "========A execution failed========"
                }
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}