
pipeline{

    agent { label 'BADRY.PC' }

    stages {
        stage('selection Options') {
            steps{
                script {
                     properties([
                        parameters([
                            choice(
                                choices: ['Installation', 'Update'],
                            
                            )
                        ])
                    ])
                }
            }
        }

        stage('deploy') {
            steps{
                echo 'building...'
            }
        }

        stage('test') {
            steps{
                echo 'building...'
            }
        }
    }
}