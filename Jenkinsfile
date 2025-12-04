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





































//move to C:\aws_keys\myserver.pem

//ssh -i C:\aws_keys\myserver.pem ubuntu@xx.xx.xx.xx


//sudo apt update


//sudo apt install -y openjdk-8-jdk


//sudo apt install -y tomcat9


//sudo systemctl start tomcat9
//sudo systemctl enable tomcat9


//scp -i C:\aws_keys\myserver.pem C:\path\to\your\warfile\myapp.war ubuntu@xx.xx.xx.xx:/home/ubuntu/


//ssh -i C:\aws_keys\myserver.pem ubuntu@xx.xx.xx.xx


//sudo mv myapp.war /var/lib/tomcat9/webapps/
//ls /var/lib/tomcat9/webapps/


//sudo systemctl restart tomcat9
//myapp
//myapp.war



//http://<EC2-IP>:8080/myapp/




















//minikube start

//kubectl create deployment mynginx --image=nginx

//kubectl get deployments
//kubectl get pods
//kubectl describe pods

//kubectl expose deployment mynginx --type=NodePort --port=80 --target-port=80

//kubectl scale deployment mynginx --replicas=4

//kubectl get svc mynginx

//kubectl port-forward svc/mynginx 8082:80


































