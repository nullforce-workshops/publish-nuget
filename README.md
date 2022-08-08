# Nullforce.ExampleNuget

An example of creating a NuGet package with:
- Publishing to GitHub packages
- Versioning via GitVersion

## NuGet Packaging

The NuGet package created from the `main` branch will:
- Create a prerelease CI package for individual commits (e.g., `NuGetExample.0.1.0-ci.0.nupkg`)
- Create a release package for tagged commits (e.g., `NuGetExample.0.1.0.nupkg`)
- Publish the package to GitHub packages
- Publish the package to nuget.org

The NuGet package created from any other branches will:
- Create a prerelease package for the branch (e.g., `NuGetExample.0.1.0-branchName.1.nupkg`)
- Publish the package to GitHub packages

## Notes on GitVersion

Requirements:
- A git repository (i.e., `git init`)
- An initial commit
