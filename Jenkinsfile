
pipeline {
    agent { label 'BADRY.PC' }

    stages {
        stage('selection Options') {
            steps {
                script {
                    // Get the input
                    def userInput = input(
                            id: 'userInput', message: 'Installation\Update',
                            parameters: [

                                choice(choices: 'Installation\nUpdate',
                                description: 'Optimizer Selection',
                                name: 'Optimizer'),

                                booleanParam(defaultValue: true, description: '', name: 'DB'),
                                booleanParam(defaultValue: true, description: '', name: 'NTP'),
                                booleanParam(defaultValue: true, description: '', name: 'ITS'),
                                booleanParam(defaultValue: true, description: '', name: 'Node.Js'),
                                booleanParam(defaultValue: true, description: '', name: 'LPR'),
                                booleanParam(defaultValue: true, description: '', name: 'VMS'),

  
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
