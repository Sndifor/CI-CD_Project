pipeline {
    agent any
    environment {
        STACK_NAME = 'DemoStack5'
        
    }
    stages {
        stage('Submit Stack') {
            steps {
                withAWS (credentials: 'Jenkins_AWSID' , region: 'us-west-1') 
                sh "aws cloudformation create-stack --stack-name $STACK_NAME -t file://ec2.yml --region 'us-east-1'"
            }
        }
    }
}
