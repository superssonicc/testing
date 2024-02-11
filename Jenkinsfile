pipeline {
    agent any
    stages {
        stage('Git checkout') {
            steps {
                git 'https://github.com/superssonicc/testing'
            }
        }

        stage('testing') {
            steps {
                sh '''
                    prophecyUpdatedLibs=$(git diff-tree --no-commit-id --name-only -r $(Build.SourceVersion) | grep "^eight/" | cut -d/ -f2 | uniq)
                    echo "updated folder are  $prophecyUpdatedLibs"
                '''
            }
        }
 
    }
}