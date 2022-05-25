
def inputOptimizer
pipeline{

    agent { label 'BADRY.PC' }

    stages {
        stage('selection Options') {
            steps{
                script {
                   def userInput = input(
                        id: 'userInput', message: 'Choose Installation/Update',
                        parameters: [

                        booleanParam(defaultValue: true, description: '', name: 'Installation'),
                        booleanParam(defaultValue: true, description: '', name: 'Update'),

                        choice(choices: 'OpenCV DNN\nOpenVino CPU\nOnnex Run-Time\nDeep Stream NVIDIA',
                        description: 'Optimizer Selection',
                        name: 'Optimizer'),
                    ])

                    inputOptimizer = userInput.Optimizer?:''

                    echo("You Choice Optimizer: ${inputOptimizer}")
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