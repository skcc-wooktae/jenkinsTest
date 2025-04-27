pipeline {
  agent any
  stages {
    stage('Buzz Buzz') {
      steps {
        echo 'Bees Buzz!'
        echo 'Fuck!'
      }
    }

    stage('Bees Bees') {
      steps {
        echo ' Buzz, Bees, Buzz!'
        echo 'tired..'
      }
    }

    stage('Lets go') {
      parallel {
        stage('chaging') {
          steps {
            echo 'hello wook'
            echo 'new branch!'
            bat 'echo hello'
            bat 'echo %Name%'
          }
        }

        stage('Parallel') {
          steps {
            bat 'mvn clean install'
            echo 'Build Success!'
          }
        }

      }
    }

  }
  environment {
    Name = 'wooktae!'
  }
}