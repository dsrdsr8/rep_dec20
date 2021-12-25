pipeline 
{
    agent any

    stages 
    {
        stage('Checkout Code') 
        {
            steps 
            {
                echo 'Checkout the files from git repo-- Worked'
				checkout scm
            }
        }
		
		stage('Build') 
        {
            steps 
            {
                echo 'Build App'
		echo 'bat mvn clean install -- thi is for Windows'
		sh mvn clean install
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
