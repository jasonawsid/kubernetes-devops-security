pipeline {
  agent any

  stages {
      stage('Build Artifact') {
            steps {
              sh "mvn clean package -DskipTests=true"
              archive 'target/*.jar' //change to trigger the pipeline
            }
        }   
      stage('Unit Tests') {
            steps {
              sh "mvn test"
            }
        }   
    }
}