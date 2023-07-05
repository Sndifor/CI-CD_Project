pipeline {
    agent any
    
    stages {
        stage('Submit Stack') {
            environment {
                STACK_NAME = 'DemoStack5'
            }
            steps {
                withAWS (credentials: 'Jenkins_AWSID' , region: 'us-west-1') {
                    sh "aws cloudformation create-stack --stack-name $STACK_NAME -t file://ec2.yml --region 'us-east-1'"
                }
                
            }
        }
        stage('Submit Stack') {
            environment {
                STACK_NAME = 'DemoStack5'
            }
            steps {
                withAWS (credentials: 'Jenkins_AWSID' , region: 'us-west-2') {
                    sh "aws cloudformation create-stack --stack-name $STACK_NAME -t file://ec2.yml --region 'us-east-1'"
                }
                
            }

        }
    }
}
