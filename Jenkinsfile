pipeline {
  agent any
  stages {
    stage('prepare env') {
      sh 'git clone https://github.com/rbenv/rbenv.git ~/.rbenv'
      sh 'cd ~/.rbenv && src/configure && make -C src'
      sh '\'echo export PATH="$HOME/.rbenv/bin:$PATH"\' >> ~/.bash_profile'
      sh 'rbenv init'
      sh 'rbenv install 2.3.1'
    }
    stage('build') {
      steps {
        sh 'ruby --version'
        sh 'bundle install'
      }
    }
  }
}
