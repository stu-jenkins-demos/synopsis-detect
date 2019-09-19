pipeline{
    agent any
    stages{
        stage('build'){
            steps{
                echo 'building'

            }
        }
        stage('test and scan') {
            parallel {
                stage('test') {
                    steps {
                        echo 'testing'
                    }
                }
                stage('scan') {
                    steps {
                        synopsys_detect 'my args'

                    }
                }
            }
        }
    
    }
    post{
            always{
                echo 'always'
            }
            success{
                echo 'success'
            }
            cleanup {
                echo 'cleaning up'
            }
        }
}
