
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

                        choice(choices: 'DB\nNTP\nITS\nNode.Js\nLPR\nVMS',
                        description: 'Select Installation ',
                        name: 'Optimizer'),
                        choice(choices: 'DB\nNTP\nITS\nNode.Js\nLPR\nVMS',
                        description: 'Select Update ',
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