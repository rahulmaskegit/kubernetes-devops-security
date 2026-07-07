stage('Build Artifact') {
    sh 'mvn clean package -DskipTests=true'
    archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
}
