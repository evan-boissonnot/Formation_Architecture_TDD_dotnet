pipeline {
     agent any
     stages {
       stage('Checkout'){
               steps {
                    bat 'echo step1'
               }
          }
       stage('build') {
          steps {
             bat 'echo step1'
             bat 'echo step2'
             bat '''
                "C:\\Program Files (x86)\\NuGet\\Visual Studio 2015\\nuget.exe" restore ${workspace}@script\\Formation.DotNet.TDD\\Formation.DotNet.TDD.sln
                "C:\\Program Files (x86)\\MSBuild\\14.0\\Bin\\msbuild.exe" ${workspace}@script\\Formation.DotNet.TDD\\Formation.DotNet.TDD.sln /t:Rebuild
                echo 'Example'
             '''
             echo 'not using shell'
          }
       }
       stage('test') {
          steps {
             bat '''
             "C:\\Program Files (x86)\\Microsoft Visual Studio 14.0\\Common7\\IDE\\mstest.exe" /testcontainer:${workspace}@script\\Formation.DotNet.TDD\\ConsoleApp1Tests\\bin\\Debug\\ConsoleApp1Tests.dll /resultsfile:${workspace}@script\\result.xml
             '''
          }
       }
     }
}
