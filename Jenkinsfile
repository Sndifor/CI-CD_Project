pipeline {
    agent any
    
    stages {
        stage('Submit Stack') {
            environment {
                STACK_NAME = 'DemoStack5'
            }
            steps {
                withAWS (credentials: 'Jenkins_AWSID' , region: 'us-east-1') {
                    sh "aws cloudformation create-stack --stack-name $STACK_NAME --template-body file://ec2.yml"
                }
                
            }
        }
        stage('Submit Stack1') {
            environment {
                STACK_NAME = 'DemoStack7'
            }
            steps {
                withAWS (credentials: 'Jenkins_AWSID' , region: 'us-east-2') {
                    sh "aws cloudformation create-stack --stack-name $STACK_NAME --template-body file://ec2.yml"
                }
                
            }

        }
    }
}
