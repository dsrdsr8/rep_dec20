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
		
<<<<<<< HEAD
       stage('Build') 
=======
	stage('Build') 
>>>>>>> 78de36acf200d21a9306d7f4b5b72724534b731d
        {
            steps 
            {
                echo 'Build App'
		echo 'bat mvn clean install -- thi is for Windows'
		echo 'linux syntas mvn clean install'
<<<<<<< HEAD
		
            }
        }

=======
		sh 'mvn clean install'
            }
        }

        stage('sonar analysis') 
        {
            steps 
            {
                echo 'In code analysis for first time'
                 withSonarQubeEnv('sonar') 
		{ 
		sh 'mvn sonar:sonar'       
		}       
            }
        }
>>>>>>> 78de36acf200d21a9306d7f4b5b72724534b731d
        stage('Nexu Upload')
        {
            steps
            {
                echo 'Nexus Upload Code'
		   
            }
        }

        stage('Deploy') 
        {
            steps 
            {
                echo 'Deploy App'
            }
        }
<<<<<<< HEAD
     }    
=======
  
    }

  
>>>>>>> 78de36acf200d21a9306d7f4b5b72724534b731d
}
