pipeline {
    agent any
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-1',credentials:'aws-static') {
		    sh 'echo "Hello World with AWS creds"'
                    s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'s3bucketforjalilproject')
                }
            }
        }
    }
}
