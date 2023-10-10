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
