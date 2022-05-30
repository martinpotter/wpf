# Contributing Guide

See also the official upstream [WPF Contributing Guide](https://github.com/dotnet/wpf/blob/main/Documentation/contributing.md).

See [Developer Guide](developer-guide.md) to learn how to develop changes for this repo.

## Contribution "Bar"

Project maintainers will consider changes that improve the product or fix known bugs (please file issues to make bugs "known").

Maintainers will not merge changes that have narrowly-defined benefits due to compatibility risk or complexity added to the product. We may revert changes if they are found to be breaking.

Most .NET Core components are cross-platform and we appreciate contributions that either improve their feature set in a given environment or that add support for a new environment. We will typically not accept contributions that implement support for an OS-specific technolology on another operating system.  We also do not intend to accept contributions that provide cross-platform implementations for Windows Forms or WPF.

Contributions must also satisfy the [acceptance criteria](acceptance_criteria.md) to learn how to develop changes for this repo.as well as other published guidelines defined in this document.

## Code Formatting Improvements and Minor Enhancements

We will consider code-formatting improvements that are identified by running code analyzers.

Our CodeAnalysis rules are not enabled by default. These can be enabled by setting the MSBuild property `EnableAnalyzers=true` (in commandline, it is set as `/p:EnableAnalyzers=true`).  

The code analyzer would likely recommend changes that can result in changes to the generated IL. In general, we prefer code-formatting PR's to be limited to changes that do not have any impact on the IL - these are easier to review and approve and do not require additional testing. 

Please open issues for changes that affect the IL or might require additional validation, and work with the project maintainers to determine whether a PR would be appropriate.
