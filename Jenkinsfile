node {
   stage('Checkout') {
       echo 'Hello from Stage 1'
       cleanWs()
      checkout scm
   }
    stage('init') {
        sh 'terraform init'
    }
    stage('plan') {
        sh 'terraform plan'
    }
     stage('Apply') {
        input 'Apply Plan'
        sh 'terraform apply -auto-approve=true'
    }
}
