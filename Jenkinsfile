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
        sh 'terraform apply'
        input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
              }
    }
}
