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
