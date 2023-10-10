pipeline {
  agent {label 'kong-build'}

  environment {
    PROJECT_NAME = 'orchsym-gateway'
    GH_TOKEN = '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'
  }

  stages {
    stage('Compile') {
      steps {
        container('kong-build') {
		sh  "make dev"
      }
    }
  }
}
}
