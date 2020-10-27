node {
   stage('Checkout') {
       echo 'Hello from Stage 1'
       cleanWs()
      checkout scm
   }
    stage('init') {
        #echo env.AWS_ACCESS_KEY_ID
        #echo env.AWS_SECRET_ACCESS_KEY
        sh 'terraform init'
    }
    stage('plan') {
        sh 'terraform plan'
    }
     stage('Apply') {
        sh 'terraform apply'
    }
}
