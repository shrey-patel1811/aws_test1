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
        script {
             def userInput = input(id: 'userInput', message: 'Merge to?',
             parameters: [[$class: 'ChoiceParameterDefinition', defaultValue: 'strDef', 
                description:'describing choices', name:'nameChoice', choices: "QA\nUAT\nProduction\nDevelop\nMaster"]
             ])

            println(userInput); //Use this value to branch to different logic if needed
        }
    }
}
