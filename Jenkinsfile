pipeline{
  agent { label 'Ajenkins' }
  tools{
    jdk 'Java17'
    maven 'Maven3'
  }
  stages{
    stage("Cleanup Workspace"){
      steps{
        cleanWs()
      }
    }
    stage("Checkout from SCM"){
      steps{
        git branch:'master',credentialsID:'github',url:'https://github.com/Mani-Bhaskar-Edula/website'
      }
    }
    stage("Build Application"){
      steps{
        sh "mvn build package"
      }
    }
    stage("Test Application"){
      steps{
        sh "mvn test application"
      }
    }
  }
}  
    
