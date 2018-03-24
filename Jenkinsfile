pipeline {
     agent any
     stages {
        stage ('Checkout') {
             steps {
                 checkout scm
             }
         }
     }
    stage ('Build') {
        steps {
            msBuild {
                buildFile('.\\Formation.DotNet.TDD\\Formation.DotNet.TDD.sln')
                passBuildVariables()
                continueOnBuildFailure()
                unstableIfWarnings()
            }
        }
    }
}
