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
      steps {
        echo 'hello wook'
        echo 'new branch!'
        bat 'echo hello'
        bat 'echo %Name%'
        sh '''echo "hello! sh"
'''
      }
    }

  }
  environment {
    Name = 'wooktae!'
  }
}