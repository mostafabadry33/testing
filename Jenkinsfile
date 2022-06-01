
def db
def ftb
def ntp
def its
def nodejs
def lpr
def vms
  
pipeline {

    agent none

    

    stages {
        stage('label list') {
            steps{
                script{

                    def nodes = []
                    jenkins.model.Jenkins.get().computers.each { c ->

                        echo "new node"
                        echo c.node.selfLabel.name

                        nodes.add(c.node.selfLabel.name)
                    }

                    env.NODE_NAME = input message: 'SELECT NODE', ok: 'Release!',
                            parameters: [choice(name: 'NODE_NAME', choices: nodes, description: 'What is the NODE TO RUN?')]

                    echo "Release scope selected: ${env.NODE_NAME}"
                      
                }
            }
        }
        stage('selection Options') {
            steps {
                script {
                    echo "Node Selected ${env.NODE_NAME}"
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
                    ])

                    install = userInput.install ?: ''
                    db = userInput.DB ?: ''
                    ftb = userInput.FTB ?: ''
                    ntp = userInput.NTP ?: ''
                    its = userInput.ITS ?: ''
                    nodejs = userInput.NODEJS ?: ''
                    lpr = userInput.LPR ?: ''
                    vms = userInput.VMS ?: ''




                    def userInput2 = input(
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
                    ])

                    update = userInput2.update ?: ''
                    db = userInput2.DB ?: ''
                    ftb = userInput2.FTB ?: ''
                    ntp = userInput2.NTP ?: ''
                    its = userInput2.ITS ?: ''
                    nodejs = userInput2.NODEJS ?: ''
                    lpr = userInput2.LPR ?: ''
                    vms = userInput2.VMS ?: ''


                }
           }
        }
        stage('Login')  {
            steps  {
                echo 'Login To DockerHub..'
                sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
            }
        }


        stage('pulling images from dockerhub') {
            steps{
                script{
                    echo "Node Selected ${env.NODE_NAME}"
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
                    if (update == "Update") {
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
