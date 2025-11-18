node {

    stage('Checkout') {
        echo "Cloning project from GitHub..."
        checkout scm
    }

    stage('Build') {
        echo "Running Maven Build..."
        bat 'mvn clean install'
        // If your Jenkins agent runs Linux:
        // sh 'mvn clean install'
    }

    stage('Test') {
        echo "Executing tests..."
        bat 'mvn test'
    }

    stage('Package JAR') {
        echo "Packaging JAR file..."
        bat 'mvn package'
    }

    stage('Archive JAR') {
        echo "Saving JAR to Jenkins Artifacts..."
        archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
    }
}
