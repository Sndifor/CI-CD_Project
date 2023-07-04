pipeline {
    agent any
    environment {
        AWS_ACCESS_KEY_ID     = 'AKIAWTRU4YRW3EKJY7GM'
        AWS_SECRET_ACCESS_KEY = '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'
    }
    stages {
        stage('Submit Stack') {
            steps {
                sh "aws cloudformation create-stack --stack-name testecinstance --template-body file://ec2.yml --tags Key=Name,Value=FirstTestInstance --region 'us-east-1'"
            }
        }
    }
}
