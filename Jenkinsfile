
pipeline {
    agent { label 'BADRY.PC' }

    stages {
        stage('selection Options') {
            steps {
                script {
                    
                    def userInput = input(
                               id: 'userInput', message: 'Installation',
                               parameters: [

                                choice(choices: 'Installation',
                                description: 'Optimizer Selection',
                                name: 'install'),

                                booleanParam(defaultValue: true, description: '', name: 'DB'),
                                booleanParam(defaultValue: true, description: '', name: 'FTB'),
                                booleanParam(defaultValue: true, description: '', name: 'NTP'),
                                booleanParam(defaultValue: true, description: '', name: 'ITS'),
                                booleanParam(defaultValue: true, description: '', name: 'NODEJS'),
                                booleanParam(defaultValue: true, description: '', name: 'LPR'),
                                booleanParam(defaultValue: true, description: '', name: 'VMS'),

                                install = userInput.install ?: ''
                                db = userInput.DB ?: ''
                                ftb = userInput.FTB ?: ''
                                ntp = userInput.NTP ?: ''
                                its = userInput.ITS ?: ''
                                nodejs = userInput.NODEJS ?: ''
                                lpr = userInput.LPR ?: ''
                                vms = userInput.VMS ?: ''
                            ])
                            if (install == "Installation") {
                              echo("installing apps")
                             if (db==true){
                              echo("installing db")
                              }
                             if (ftb==true){
                              echo("installing ftb")
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

                    def userInput = input(
                               id: 'userInput', message: 'Update',
                               parameters: [

                                choice(choices: 'Update',
                                description: 'Optimizer Selection',
                                name: 'update'),

                                booleanParam(defaultValue: false, description: '', name: 'DB'),
                                booleanParam(defaultValue: false, description: '', name: 'FTB'),
                                booleanParam(defaultValue: false, description: '', name: 'NTP'),
                                booleanParam(defaultValue: false, description: '', name: 'ITS'),
                                booleanParam(defaultValue: false, description: '', name: 'NODEJS'),
                                booleanParam(defaultValue: false, description: '', name: 'LPR'),
                                booleanParam(defaultValue: false, description: '', name: 'VMS'),

                                update = userInput.update ?: ''
                                db = userInput.DB ?: ''
                                ftb = userInput.FTB ?: ''
                                ntp = userInput.NTP ?: ''
                                its = userInput.ITS ?: ''
                                nodejs = userInput.NODEJS ?: ''
                                lpr = userInput.LPR ?: ''
                                vms = userInput.VMS ?: ''
                            ])


                            if (install == "Update") {
                               echo("updating apps")
                             if (db==true){
                              echo("updating db")
                               }
                             if (ftb==true){
                              echo("updating ftb")
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
