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
