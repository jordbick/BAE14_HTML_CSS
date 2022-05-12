pipeline{
        agent any
        stages{
            stage('Clone repo'){
                steps{
                    git branch: 'main', url: 'https://github.com/jordbick/scriptrepo.git'
                }
            }
            stage('Run script'){
                steps{
                    sh 'sh ./myscript.sh'
                }
            }
            stage('Archive'){
                steps{
                   archiveArtifacts artifacts: 'output', followSymlinks: false
                        }
                }
        }
}
