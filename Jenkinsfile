pipeline {
    agent any
    environment {
        AWS_ACCESS_KEY_ID     = 'AKIAWTRU4YRW3EKJY7GM'
        AWS_SECRET_ACCESS_KEY = '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'
    }
    stages {
        stage('Submit Stack') {
            steps {
                sh "aws cloudformation create-stack --stack-name DemoStack5 --template-body file://ec2.yml --region 'us-east-1'"
            }
        }
    }
}
