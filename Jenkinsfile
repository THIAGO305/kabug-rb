pipeline{
    agent {
        docker {
            image 'ruby'
        }
    }
    stages{
        stage('Build'){
            steps{
                echo 'Buildins or Resolver Dependencies teste'
            }
        }
    stage('Test'){
            steps{
                echo 'Running regression tests'
            }
        }
    stage('UAT'){
            steps{
                echo 'Wait for User Accetance'
                input(message:'Go to production', ok: 'Yes')
            }
        }
    stage('Prod'){
        steps{
                echo 'WebApp is Ready :)'
            }
        }
    }
}
