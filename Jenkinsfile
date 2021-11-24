pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Hello'
        git(credentialsId: 'bf60d0f3-c7f6-4474-9562-7dae9a05a806', url: 'https://github.com/mskuratowski/DevOpsWorkshops.git', branch: 'master')
        dotnetRestore()
        dotnetBuild(configuration: 'Release')
        dotnetPublish(configuration: 'Release')
      }
    }

    stage('TEST') {
      steps {
        sh 'echo "Hello"'
      }
    }

  }
}