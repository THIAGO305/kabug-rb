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
                sh 'rm -f Gemfile.lock'
                sh 'bundle install'
            }
        }
    stage('Test'){
            steps{
                echo 'Running regression tests'
                sh 'bundle exec cucumber -p ci'
                cucumber customCssFiles: '', customJsFiles: '', failedFeaturesNumber: -1, failedScenariosNumber: -1, failedStepsNumber: -1, fileIncludePattern: '**/*.json', pendingStepsNumber: -1, reportTitle: 'logs', skippedStepsNumber: -1, sortingMethod: 'ALPHABETICAL', undefinedStepsNumber: -1
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
