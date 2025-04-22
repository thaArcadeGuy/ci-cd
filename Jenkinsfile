pipeline {
  agent any
  stages {
    stage ("Setup") {
      steps {
        sh "python -m venv venv"
        sh ". venv/bin/activate"
        sh "pip install -r requirements.txt"
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