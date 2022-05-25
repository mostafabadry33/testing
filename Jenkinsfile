
pipeline{

    agent { label 'BADRY.PC' }

    stages {

        stage('build') {
            steps{
                script{
                  properties([
                        parameters([
                            choice(
                                choices: ['Installtion', 'Update'], 
                                name: 'PARAMETER_01'
                            ),
                            booleanParam(
                                defaultValue: true, 
                                description: '', 
                                name: 'BOOLEAN'
                            ),
                            text(
                                defaultValue: '''
                                this is a multi-line 
                                string parameter example
                                ''', 
                                 name: 'MULTI-LINE-STRING'
                            ),
                            string(
                                defaultValue: 'scriptcrunch', 
                                name: 'STRING-PARAMETER', 
                                trim: true
                            )
                        ])
                    ])
                }
                echo 'building...'
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