
pipeline {
    agent { label 'BADRY.PC' }

    stages {
        stage('selection Options') {
            steps {
                script {
                    // Get the input
                    def userInput = input(
                            id: 'userInput', message: 'Choose H/W Optimization!',
                            parameters: [

                                booleanParam(defaultValue: true, description: '', name: 'installation'),
                                
                                choice(choices: 'DB\nNTP\nITS\nNode.Js\nLPR\nVMS',
                                description: 'Optimizer Selection',
                                name: 'Optimizer'),

                                booleanParam(defaultValue: true, description: '', name: 'update'),

                                choice(choices: 'DB\nNTP\nITS\nNode.Js\nLPR\nVMS',
                                description: 'Optimizer Selection',
                                name: 'Optimizer'),
                            ])

                    // Save to variables. Default to empty string if not found.
                    inputOptimizer = userInput.Optimizer ?: ''

                    // Echo to console
                    echo("You Choice Optimizer: ${inputOptimizer}")
                }


            }
        }
    }
}
