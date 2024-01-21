pipeline {
  agent any

  stages {
      stage('Build Artifact') {
            steps {
              sh "mvn clean package -DskipTests=true"
              archive 'target/*.jar' // new changes
            }
        }
      stage('test') {
            steps {
              sh "mvn test"
            }
        }      
    }
}