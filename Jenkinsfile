pipeline { 
    agent any 
    tools { 
          maven 'Maven' //Ensure name matches with configured  
    } 
    stages { 
        stage('Checkout') {  
            steps { 
                git branch: 'master', url: 'https://github.com/Darshantalawar/hello.git'  
            } 
    } 
     stage('Build') {  
            steps { 
                bat 'mvn clean package'  
            } 
      } 
     stage('Test') {  
            steps { 
                bat 'mvn test'  
            } 
      } 
    stage('Run Application') {
            steps {
        bat 'java -jar target/helllo-0.0.1-SNAPSHOT.jar'
    }
 }
          
}
