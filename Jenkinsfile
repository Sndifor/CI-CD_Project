pipeline {
    agent any
    
    stages {
        stage('Submit Stack') {
            environment {
                STACK_NAME = 'DemoStack3'
            }
            steps {
                withAWS (credentials: 'Jenkins_AWSID' , region: 'us-west-1') {
                    sh "aws cloudformation create-stack --stack-name $STACK_NAME --template-body file://ec2.yml"
                }
                
            }
        }
        stage('Submit Stack1') {
            environment {
                STACK_NAME = 'DemoStack4'
            }
            steps {
                withAWS (credentials: 'Jenkins_AWSID' , region: 'us-west-1') {
                    sh "aws cloudformation create-stack --stack-name $STACK_NAME --template-body file://ec2.yml"
                }
                
            }

        }
    }
}
