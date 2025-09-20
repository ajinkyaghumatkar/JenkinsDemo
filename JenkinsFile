pipeline{
 //any available agent 
  agent any 
    
  tools{
      maven 'mymaven'
  }
    
  stages{
        stage('Checkout Code'){
            steps{
            git 'https://github.com/ajinkyaghumatkar/DevOpsCodeDemo.git'
            }
         }  
        stage(' Code Review'){
            steps{
                sh 'mvn pmd:pmd'
                
			}
		}
        stage('Compile Code'){
            steps{
                sh 'mvn compile'
            }
         }   
        stage('Test Code'){
            steps{
                sh 'mvn test'
                
            }
         }   
        stage('Package Code'){
            steps{
                sh 'mvn package'
                
            }
        }    
      
      
  }
}
