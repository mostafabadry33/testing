
pipeline{

    agent { label 'BADRY.PC' }

    stages {
        stage('selection Options') {
            steps{
                script {
                    parameters {
                     checkboxParameter(name: 'Platforms1', format: 'JSON',
                     pipelineSubmitContent: '{"CheckboxParameter": [{"key": "nt","value": "nt"},{"key": "linux","value": "linux"},{"key": "unix","value": "unix"}]}', description: '')
                     checkboxParameter(name: 'Platforms2', format: 'YAML',
                     pipelineSubmitContent: "CheckboxParameter: \n  - key: monday\n    value: monday\n  - key: tuesday\n    value: tuesday\n", description: '')
                    }
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