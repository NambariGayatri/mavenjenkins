pipeline 
{
    agent any

    stages 
    {
        stage('CheckOut') 
	    {
           git 'https://github.com/NambariGayatri/mavenjenkins.git'
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

    post
    {

    	always
    	{
    		emailext body: 'Summary', subject: 'Pipeline Status', to: 'gayatri.nambari@gmail.com'
    	}

    }
}
