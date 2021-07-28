//Testing to know changes on jenkins
pipeline {
    agent any
    stages {
       stage('build') {
          steps {
             echo 'Notify GitHUb'
             updateGithubCommitStatus name: 'build', state: 'pending'
             echo 'build step goes here'
             updateGithubCommitStatus name: 'build', state: 'success'
          }
       }
       stage(test) {
           steps {
               echo 'Notify GitLab'
               updateGithubCommitStatus name: 'test', state: 'pending'
               echo 'test step goes here'
               updateGithubCommitStatus name: 'test', state: 'success'

           }
       }
    }
 }
