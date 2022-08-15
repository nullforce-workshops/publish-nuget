# Nullforce.Example.NuGetExample

An example of creating a NuGet package with:
- Publishing to GitHub packages
- Versioning via GitVersion

| Build | NuGet | NuGet (prerelease) |
|-------|-------|--------------------|
| [![Build Status][buildbadge]][buildurl] | [![nuget][nugetbadge]][nugeturl] | [![nuget prerelease][nugetprebadge]][nugetpreurl] |


## NuGet Packaging

The NuGet package created from the `main` branch will:
- Create a prerelease CI package for individual commits (e.g., `Nullforce.Example.NuGetExample.0.1.0-ci.0.nupkg`)
- Create a release package for tagged commits (e.g., `Nullforce.Example.NuGetExample.0.1.0.nupkg`)
- Publish the package to GitHub packages
- Publish the package to nuget.org

The NuGet package created from any other branches will:
- Create a prerelease package for the branch (e.g., `Nullforce.Example.NuGetExample.0.1.0-branchName.1.nupkg`)
- Publish the package to GitHub packages

## Notes on GitVersion

Requirements:
- A git repository (i.e., `git init`)
- An initial commit

[buildbadge]: https://github.com/nullforce-workshops/publish-nuget/workflows/build/badge.svg?branch=main
[buildurl]: https://github.com/nullforce-workshops/publish-nuget/actions/
[nugetbadge]: https://img.shields.io/nuget/v/Nullforce.Example.NuGetExample.svg
[nugeturl]: https://www.nuget.org/packages/Nullforce.Example.NuGetExample/
[nugetprebadge]: https://img.shields.io/nuget/vpre/Nullforce.Example.NuGetExample.svg
[nugetpreurl]: https://www.nuget.org/packages/Nullforce.Example.NuGetExample/
