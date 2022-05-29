# Faithlife.WPF

[![Build Status](https://dev.azure.com/Faithlife/WPF/_apis/build/status/Faithlife.wpf?branchName=stable)](https://dev.azure.com/Faithlife/WPF/_build/latest?definitionId=11&branchName=stable) [![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/Faithlife/wpf/blob/stable/LICENSE.TXT)

This is a custom build of [Windows Presentation Foundation](https://github.com/dotnet/wpf) maintained by [Faithlife](https://faithlife.codes/).

## Getting started

### Consuming

To use Faithlife.Wpf, build a regular WPF application (`dotnet new wpf`), then add a package reference to Faithlife.Wpf. The assemblies from this package should take precedence over the ones from .NET 6.

### Building

* To build a dev package: `build.cmd -c Release -platform x64 -test -pack`
  * To use a unique version number, add `/p:OfficialBuildId=YYYYMMDD.BUILD`, e.g., `/p:OfficialBuildId=20220324.5`.
* All commits pushed to the `stable` branch will build a CI package. To ship the package, find the correct [build in Azure Pipelines](https://dev.azure.com/Faithlife/WPF/_build?definitionId=11&_a=summary), download the "nupkg" artifact, and upload it to NuGet.org.
* [Contributing guide](Documentation/contributing.md)

## Issues

Open an issue on this repo for problems _specifically with_ this package. All other issues should be opened on [dotnet/wpf](https://github.com/dotnet/wpf/issues).

## License

WPF is licensed under the [MIT license](LICENSE.TXT).
