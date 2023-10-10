pipeline {
  agent {label 'kong-build'}

  environment {
    PROJECT_NAME = 'orchsym-gateway'
  }

  stages {
    stage('Compile') {
      steps {
        container('kong-build') {
            sh "make dev"
            sh "make build-release"
            sh "bin/bazel build --config release :kong_el7"
        }
      }
    }
  }
}
