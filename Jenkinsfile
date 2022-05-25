def testParam = checkBox("opt", // name
                "opt1,opt2,opt3", // values
                "opt1", //default value
                0, //visible item cnt
                "Multi-select", // description
                )
pipeline{

    agent { label 'BADRY.PC' }

    stages {

        stage('build') {
            steps{
                script{
                  properties(
                  [parameters([testParam])]
                  )
                }
                echo 'building...'
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