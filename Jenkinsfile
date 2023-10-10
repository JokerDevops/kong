pipeline {
  agent {label 'kong-build'}

  environment {
    PROJECT_NAME = 'orchsym-gateway'
  }

  stages {
    stage('NOCI check') {
      steps {
        noci action: 'check'
        load_envs_common()
      }
    }

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
