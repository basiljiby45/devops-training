pipleline{
  agent any

  stages{
    stages('Checkout Code'){
      steps{
        echo 'Pulling code from Github'
        checkoutscm
      }
    }
    stage('Build Docker Image'){
      steps{
        echo 'Building Docker Image'
        bat 'docker build -t devops-training .'
      }
    }
    stage('Run docker container'){
      steps{
        echo'Running Docker container'
        bat 'docker run -d -p 8070:80 devops-training'
        }
      }
    }
}
