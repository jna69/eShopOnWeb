pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'dotnet build eShopOnWeb.sln'
      }
    }

    stage('Unit') {
      steps {
        sh 'dotnet test tests/UnitTests'
      }
    }

    stage('Integration') {
      steps {
        sh 'dotnet test tests/IntegrationTests'
      }
    }

    stage('Functionnal') {
      steps {
        sh 'dotnet test tests/FunctionalTests'
      }
    }

    stage('Deployment') {
      steps {
        sh 'dotnet publish eShopOnWeb.sln'
      }
    }

  }
}