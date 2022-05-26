
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
                        db = userInput.DB ?: ''
                        ntp = userInput.NTP ?: ''
                        its = userInput.ITS ?: ''
                        node.js = userInput.Node.Js ?: ''
                        lpr = userInput.LPR ?: ''
                        vms = userInput.VMS ?: ''
                        if (install == "Installation") {
                         
                          echo("installing apps")
                          if (db==true){
                              echo("installing DB")

                          }
                          if (ntp==true){
                              echo("installing ntp")

                          }
                          if (its==true){
                              echo("installing its")
                        }
                          if (node.js==true){
                              echo("installing node.js")
                        }
                          if (lpr==true){
                              echo("installing lpr")
                        }
                            if (vms==true){
                              echo("installing vms")
                        }
                        if (install == "Update") {
                         
                          echo("updating apps")
                          if (db==true){
                              echo("updating db")

                          }
                          if (ntp==true){
                              echo("updating ntp")

                          }
                        }   
                    //inputOptimizer = userInput.install ?: ''

                    //echo("You Choice Selection: ${inputOptimizer}")
                }
           }
        }
    }
}
