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
          sh "echo $GH_TOKEN"
		sh 	 "make dev"
      }
    }
  }
}
}
