pilpeline{
    agent{ docker 'maven:3.5-alpine'}
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
