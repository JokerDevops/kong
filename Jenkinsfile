pipeline {
  agent {label 'kong-build'}

  environment {
    PROJECT_NAME = 'orchsym-gateway'
    GH_TOKEN = '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'
    GITHUB_TOKEN = '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'
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
