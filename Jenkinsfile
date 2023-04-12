pipeline {
  agent any
  stages {
    stage('static') {
      steps {
        script {
          pipeline {
            agent any

            stages {
              stage('Static Analysis') {
                steps {
                  withSonarQubeEnv('SonarQube') {
                    sh 'mvn clean verify sonar:sonar'
                  }
                }
              }
            }
          }
        }

      }
    }

  }
}