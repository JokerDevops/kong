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
