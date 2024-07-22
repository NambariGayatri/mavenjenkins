pipeline 
{
    agent any

    stages 
    {
       stage('CheckOut') 
	{
            steps 
	    {
                git 'https://github.com/NambariGayatri/mavenjenkins.git'
            }
        }
        stage('Build') 
        {
            steps 
            {
                echo 'Build App'
            }
        }

        stage('Test') 
        {
            steps 
            {
                echo 'Test App'
            }
        }

        stage('Deploy') 
        {
            steps 
            {
                echo 'Deploy App'
            }
        }
    }

   post {
        always {
            emailext(
                subject: "Pipeline status: ${BUILD_NUMBER}",
                body: """<html>
                            <body>
                                <p>Build Status: ${BUILD_STATUS}</p>
                                <p>Build Number: ${BUILD_NUMBER}</p>
                                <p>Build URL: <a href="${BUILD_URL}">${BUILD_URL}</a></p>
                            </body>
                        </html>""",
                to: 'gayatri.nambari@gmail.com',
                from: 'jenkins@example.com',
                replyTo: 'jenkins@example.com',
                mimeType: 'text/html'
    	}

    }
}
}	
