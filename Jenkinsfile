pipeline {
  agent none
  stages {
    stage('Buzz Buzz') {
      agent {
        node {
          label 'jdk11'
        }

      }
      steps {
        echo 'Bees Buzz!'
        echo 'Fuck!'
      }
    }

    stage('Bees Bees') {
      agent {
        node {
          label 'jdk21'
        }

      }
      steps {
        echo ' Buzz, Bees, Buzz!'
        echo 'tired..'
      }
    }

    stage('Lets go') {
      parallel {
        stage('chaging') {
          agent any
          steps {
            echo 'hello wook'
            echo 'new branch!'
            bat 'echo hello'
            bat 'echo %Name%'
          }
        }

        stage('Parallel') {
          agent any
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