# Faithlife.WPF

[![Build Status](https://dev.azure.com/Faithlife/WPF/_apis/build/status/Faithlife.wpf?branchName=stable)](https://dev.azure.com/Faithlife/WPF/_build/latest?definitionId=11&branchName=stable) [![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/Faithlife/wpf/blob/stable/LICENSE.TXT)

This is a custom build of [Windows Presentation Foundation](https://github.com/dotnet/wpf) maintained by [Faithlife](https://faithlife.codes/).
The `stable` branch (6.x) is based off the `release/6.0` branch and is suitable to use with .NET 6.0 applications. The `master` branch (7.x) tracks .NET 7.0 and is suitable for pre-release testing.
The [Release Notes](ReleaseNotes.md) list the differences from the official release.

See the [WPF Roadmap](roadmap.md) to learn about project priorities, status and ship dates.

### Consuming

To use Faithlife.Wpf, build a regular WPF application (`dotnet new wpf`). Add the [Faithlife WPF package feed](https://dev.azure.com/Faithlife/WPF/_artifacts/feed/Public)
to your `NuGet.config`:

```xml
<configuration>
  <packageSources>
    <add key="Faithlife WPF" value="https://pkgs.dev.azure.com/Faithlife/WPF/_packaging/Public/nuget/v3/index.json" />
  </packageSources>
</configuration>
```

In your CSPROJ file, update the Microsoft.WindowsDesktop.App reference:

```xml
<ItemGroup>
  <FrameworkReference Update="Microsoft.WindowsDesktop.App" RuntimeFrameworkVersion="6.0.6-faithlife.1.22304.12" />
</ItemGroup>
```

### Building

* To build a dev package: `build.cmd -c Release -platform x64 -test -pack`
  * To use a unique version number, add `/p:OfficialBuildId=YYYYMMDD.BUILD`, e.g., `/p:OfficialBuildId=20220324.5`.
* All commits pushed to the `stable` branch will build a CI package that will be pushed to the Azure Artifacts feed.
* [Contributing guide](Documentation/contributing.md)

## Issues

Open an issue on this repo for problems _specifically with_ this package. All other issues should be opened on [dotnet/wpf](https://github.com/dotnet/wpf/issues).

## License

WPF is licensed under the [MIT license](LICENSE.TXT).
