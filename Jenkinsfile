node {
	stage 'Checkout'
		checkout scm

	stage 'Build'
		bat """ "C:\\Program Files (x86)\\NuGet\\Visual Studio 2015\\nuget.exe" restore .\\Formation.DotNet.TDD\\Formation.DotNet.TDD.sln """
}
