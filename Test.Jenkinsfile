pipeline {
  agent any
  parameters {
    // App List Parameters -> automatically filled by LT Trigger plugin
    string(name: 'ApplicationScope', defaultValue: '', description: 'Comma- deploy.')
    string(name: 'TriggeredBy', defaultValue: 'N/A', description: 'Namremotely.')
  }
  stages {
      stage('GitHubExecution') {
            steps {
              echo "Githubへの疎通"
              build 'FromGithub2'
            }
      }
      stage('python実行') {
            steps {
              echo "pythonコード実行処理"
              build quietPeriod: 5, job: 'executepython'
            }
      }
        
    }
  
}
