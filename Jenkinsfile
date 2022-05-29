
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
                                booleanParam(defaultValue: false, description: '', name: 'NODEJS'),
                                booleanParam(defaultValue: false, description: '', name: 'LPR'),
                                booleanParam(defaultValue: false, description: '', name: 'VMS'),
                            ])
                        install = userInput.install ?: ''
                        db = userInput.DB ?: ''
                        ntp = userInput.NTP ?: ''
                        its = userInput.ITS ?: ''
                        nodejs = userInput.NODEJS ?: ''
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
                          if (nodejs==true){
                              echo("installing nodejs")
                            }
                          if (lpr==true){
                              echo("installing lpr")
                            }
                            if (vms==true){
                              echo("installing vms")
                            }
                        }
                        if (install == "Update") {
                          echo("updating apps")
                          if (db==true){
                              echo("updating DB")
                            }
                          if (ntp==true){
                              echo("updating ntp")
                            }
                          if (its==true){
                              echo("updating its")
                            }
                          if (nodejs==true){
                              echo("updating nodejs")
                            }
                          if (lpr==true){
                              echo("updating lpr")
                            }
                            if (vms==true){
                              echo("updating vms")
                            }
                    }
                }
           }
        }
    }
}
