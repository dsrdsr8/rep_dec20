pipeline 
{
    agent any

    stages 
    {
        stage('Checkout Code') 
        {
            steps 
            {
                echo 'Build App'
				checkout scm
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

    post
    {

    	always
    	{
    		echo 'build completed'    	}

    }
}
