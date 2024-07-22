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
                subject: "Pipeline status: ${currentBuild.number}",
                body: """<html>
                            <body>
                                <p>Build Status: ${currentBuild.currentResult}</p>
                                <p>Build Number: ${currentBuild.number}</p>
                                <p>Build URL: <a href="${env.BUILD_URL}">${env.BUILD_URL}</a></p>
                            </body>
                        </html>""",
                to: 'gayatri.nambari@gmail.com',
                from: 'jenkins@example.com',
                replyTo: 'jenkins@example.com',
                mimeType: 'text/html'
    	)

    }
}
}	
