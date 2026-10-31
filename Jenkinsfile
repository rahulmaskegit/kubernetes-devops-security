pipeline {

    agent any
    stages {
    stage('Build Artifact') {
    steps {
    sh 'mvn clean package -DskipTests=true'
    archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true  //sothat
}
}

    stage('Junit-test') {
    steps {
    sh 'mvn test'
}
post {
  always {
      junit 'target/surefire-reports/*.xml'
      jacoco execPattern: 'target/jacoco.exec'
  }
}
    
    
    }
}    
}
