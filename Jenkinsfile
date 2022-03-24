pilpeline{
   agent any
    tools { 
        maven 'Maven 3.3.9' 
        jdk 'jdk8' 
    }
    stages{
        stage('checkout'){
            steps{
                git 'https://github.com/anilkumarreddy2000/24.git'
            }
        }
        stage('Build'){
            steps{
                sh 'mvn clean package'
                junit '**/target/surefire-reports/TEST-*.xml'
            }
        }
    }
}
