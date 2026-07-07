stage('Build Artifact') {
  steps {
    sh 'mvn clean package -DskipTests=true'
  }
  post {
      success {
        archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
      }
  }
}

