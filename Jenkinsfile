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
	stage('Building image') 
	    {
      	steps{
        script 	{
          app = docker.build + ":$BUILD_NUMBER"
        	}
      	     }	
    	   }
	    
        stage('Nexu Upload')
        {
            steps
            {
                echo 'Nexus Upload Code'
		nexusArtifactUploader artifacts: [[artifactId: 'spring-boot-starter-parent', classifier: '', file: '/home/skanisamca11/.jenkins/workspace/J2/target/${pom.artifactId}-${pom.version}.${pom.packaging}', type: 'jar']], credentialsId: '', groupId: 'org.springframework.boot', nexusUrl: '34.93.113.226:8081', nexusVersion: 'nexus3', protocol: 'http', repository: 'maven-snapshots', version: '1.2.2.RELEASE'
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
