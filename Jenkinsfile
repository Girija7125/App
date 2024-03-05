pipeline{
  agent{label'Jenkins-Agent'}
  tools{
    jdk 'Java17'
    maven 'Maven3'
  }
  stages{
    stage("Cleanup Workspace"){
      steps{
        cleanWS()
      }
    }
    stage("Checkout from Scm"){
      steps{
      git branch:'main',credentialsId:'github',url:'https://github.com/Girija7125/App.git'
    }
    }
    stage("Build Application"){
      steps{
        sh "mvn clean package"
      }
    }
    stage("Test Application"){
      steps{
        sh "mvn test"
      }
    }
  }
}
