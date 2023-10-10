pipeline {
  agent {label 'kong-build'}

  environment {
    PROJECT_NAME = 'orchsym-gateway'
  }

  stages {
    stage('Compile') {
      steps {
        container('kong-build') {
            script {
    		def GH_TOKEN = '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'
		make dev
		}
        }
      }
    }
  }
}
