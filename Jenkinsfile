pipeline {
     agent any
     stages {
       stage('build') {
          steps {
             bat 'echo step1'
             bat 'echo step2'
             bat '''
                "C:\\Program Files (x86)\\NuGet\\Visual Studio 2015\\nuget.exe" restore .\\Formation.DotNet.TDD\\Formation.DotNet.TDD.sln
                "C:\\Program Files (x86)\\MSBuild\\14.0\Bin\\msbuild.exe" .\\Formation.DotNet.TDD\\Formation.DotNet.TDD.sln /t:build
                echo 'Example'
             '''
             echo 'not using shell'
          }
       }
     }
}
