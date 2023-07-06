pipeline {
    agent any
parameters {
            credentials credentialType: 'com.cloudbees.jenkins.plugins.awscredentials.AWSCredentialsImpl', defaultValue: '', description: 'Which Credential would you want to use for this region', name: 'AWSID', required: true
}
    stages {
        stage('Submit Stack') {
       
            environment {
                STACK_NAME = 'DemoStack3'
            }
            steps {
                sh "aws cloudformation create-stack --stack-name $STACK_NAME --template-body file://ec2.yml"
            }
        }

        stage('Submit Stack1') {
            environment {
                STACK_NAME = 'DemoStack4'
            }
            steps {
                withAWS (credentials: 'Jenkins_AWSID' , region: 'us-east-2') {
                    sh "aws cloudformation create-stack --stack-name $STACK_NAME --template-body file://ec2.yml"
                }
                
            }

        }
    }
}
