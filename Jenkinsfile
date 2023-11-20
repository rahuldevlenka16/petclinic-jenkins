pipeline{
  agent any
  stages{

    stage('Git checkout'){
      steps{
        git branch: 'main', credentialsId: '0e68a689-a831-4c94-98e1-8c488f6fadf9', url: 'https://github.com/rahuldevlenka16/petclinic-jenkins.git'
      }
    }

    // stage('unit testing'){
    //   steps{
    //     bat 'mvn test'
    //   }
    // }
    
    stage('Maven build') {
      steps {
          bat 'mvn clean package-DskipTests -Dcheckstyle.skip'
      }
    }
  }
  
}
