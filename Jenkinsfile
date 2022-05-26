
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
                        if (install == "Installation") {
                         // tmp_param =  sh (script: 'most amazing shell command', returnStdout: true).trim()
                          echo("installing apps")
                        }    
                        if (install == "Update") {
                         // tmp_param =  sh (script: 'most amazing shell command', returnStdout: true).trim()
                          echo("updating apps")
                        }   
                    //inputOptimizer = userInput.install ?: ''

                    //echo("You Choice Selection: ${inputOptimizer}")
                }
           }
        }
    }
}
