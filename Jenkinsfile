pipeline {
    agent any
    
    stages {
        stage('Submit Stack') {
            environment {
                STACK_NAME = 'DemoStack6'
            }
            steps {
                withAWS (credentials: 'Jenkins_AWSID' , region: 'us-west-1') {
                    sh "aws cloudformation create-stack --stack-name $STACK_NAME --template-body file://ec2.yml --region 'us-east-1'"
                }
                
            }
        }
    }
}
