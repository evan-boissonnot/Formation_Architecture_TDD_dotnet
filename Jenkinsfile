node {
	stage 'Checkout'
		checkout scm

	stage 'Build'
		bat """ "C:\\Program Files (x86)\\NuGet\\Visual Studio 2015\\nuget.exe" restore .\\Formation.DotNet.TDD\\Formation.DotNet.TDD.sln """
		bat "\"${tool 'MSBuild v4.5'}\" .\\Formation.DotNet.TDD\\Formation.DotNet.TDD.sln /p:Configuration=Debug /p:Platform=\"Any CPU\" /p:ProductVersion=1.0.0.${env.BUILD_NUMBER}"


}

pipeline {
    agent any
    stages {
        stage ('Checkout') {
            steps {
                checkout scm
            }
        }
	stage ('Build') {
            steps {
                bat """ "C:\\Program Files (x86)\\NuGet\\Visual Studio 2015\\nuget.exe" restore .\\Formation.DotNet.TDD\\Formation.DotNet.TDD.sln """
		bat "\"${tool 'MSBuild v4.5'}\" .\\Formation.DotNet.TDD\\Formation.DotNet.TDD.sln /p:Configuration=Debug /p:Platform=\"Any CPU\" /p:ProductVersion=1.0.0.${env.BUILD_NUMBER}"
            }
        } 
    }
}
