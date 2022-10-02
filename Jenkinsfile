pipeline {
    agent any

    stages{
        stage('deploy to S3'){
            steps{
               sh 'aws s3 cp public s3://junglemeet-20221002 --recursive'
               sh 'aws s3api put-bucket-policy --bucket junglemeet-20221002 --policy file://policy.json'
               sh 'aws s3 website s3://junglemeet-20221002/ --index-document index.html --error-document error.html'
             
            }
        }
    }
    
}
