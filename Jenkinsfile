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
          agent {
            node {
              label 'jdk11'
            }

          }
          steps {
            echo 'hello wook'
            echo 'new branch!'
            bat 'echo hello'
            bat 'echo %Name%'
          }
        }

        stage('Parallel') {
          agent {
            node {
              label 'jdk11'
            }

          }
          steps {
            bat 'mvn clean install'
            echo 'Build Success!'
          }
        }

      }
    }

    stage('stage input') {
      steps {
        input(message: 'deploy?', ok: 'yes')
      }
    }

    stage('execute java') {
      agent {
        node {
          label 'jdk11'
        }

      }
      steps {
        bat 'java -jar firstproject-0.0.1-SNAPSHOT.war'
      }
    }

  }
  environment {
    Name = 'wooktae!'
  }
}