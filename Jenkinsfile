pipeline {
  agent any
  stages {
    stage ("Setup") {
      steps {
        sh "python3 -m venv venv"
        sh ". venv/bin/activate"
        sh "pip3 install -r requirements.txt"
      }
    }
    stage ("Test") {
      steps {
        sh ". venv/bin/activate"
        sh "pytest"
      }
    }
  }
}