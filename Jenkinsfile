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
                    sh 'chmod +x myscript'
sh './myscript'
                }
            }
            stage('Archive file'){
                steps{
                    archiveArtifact artifacts: 'output'
                        }
                }
        }
}
