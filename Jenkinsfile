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
		echo 'linux syntas mvn clean install'
		
            }
        }

        stage('sonar analysis') 
        {
            steps 
            {
                echo 'In code analysis for first time'
                        
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

  
}
