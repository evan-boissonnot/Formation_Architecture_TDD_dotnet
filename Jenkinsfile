job('example') {
    steps {
        msBuild {
            buildFile('.\Formation.DotNet.TDD\Formation.DotNet.TDD.sln')
            passBuildVariables()
            continueOnBuildFailure()
            unstableIfWarnings()
        }
    }
}
