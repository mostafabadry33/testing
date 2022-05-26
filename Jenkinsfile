
pipeline {
    agent { label 'BADRY.PC' }

    stages {
        stage('selection Options') {
            steps {
                script {
                    // Get the input
                    def userInput = input(
                            id: 'userInput', message: 'Installation\nUpdate',
                            parameters: [

                                choice(choices: 'Installation\nUpdate',
                                description: 'Optimizer Selection',
                                name: 'install'),

                                booleanParam(defaultValue: false, description: '', name: 'DB'),
                                booleanParam(defaultValue: false, description: '', name: 'NTP'),
                                booleanParam(defaultValue: false, description: '', name: 'ITS'),
                                booleanParam(defaultValue: false, description: '', name: 'Node.Js'),
                                booleanParam(defaultValue: false, description: '', name: 'LPR'),
                                booleanParam(defaultValue: false, description: '', name: 'VMS'),
                            ])
                        install = userInput.install ?: ''
                        echo(install)
                    //inputOptimizer = userInput.install ?: ''

                    //echo("You Choice Selection: ${inputOptimizer}")
                }
           }
        }
    }
}
