pipeline {
  agent {label 'kong-build'}

  environment {
    PROJECT_NAME = 'orchsym-gateway'
  }

  stages {
    stage('Compile') {
      steps {
        container('kong-build') {
	  sh "export GH_TOKEN=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"
	  sh "make dev"
      }
    }
  }
}
}
