pipeline{
  agent any // significa que usará cualquier nodo para construir un pipeline
  tools{
    maven 'Maven Apache'
  }
  stages{
    stage('Chekout'){
      steps{
        //clonar repositorio desde github
        git url: 'https://github.com/desalove39/Filtrador-de-numeros-de-lista.git', branch: 'main'
      }
    }
    stage('Build') {
      steps {
        // Compilar el proyecto usando Maven
        sh 'mvn clean install'
      }
    }
  }
  post {
    success {
      echo 'Build completed successfully!'
    }
    failure {
      echo 'Build failed.'
    }
  }
}
