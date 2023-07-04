pipeline {
    agent any
    stages {
        stage('Submit Stack') {
            steps {
                sh "aws cloudformation create-stack --stack-name testecinstance --template-body file://ec2.yml --tags Key=Name,Value=FirstTestInstance"
            }
        }
    }
}
