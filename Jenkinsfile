pipeline{
    agent {
        docker {
            image 'qaninja/rubywd'
        }
    }
    stages{
        stage('Build'){
            steps{
                echo 'Buildins or Resolver Dependencies teste'
                sh 'bundle install'
            }
        }
    stage('Test'){
            steps{
                echo 'Running regression tests'
                sh 'bundle exec cucumber -p ci'
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
