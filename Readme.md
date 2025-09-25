My First Repo

pipeline {

  agent any

  stages {

    stage('Hello1') {

      steps {

        sh 'echo hello1'

      }

    }

    stage('sleep') {

      steps {

        sh 'sleep 60'

      }

    }

    stage('Hello2') {

      steps {

        sh 'echo hello2'

      }

    }

  }

}
 
