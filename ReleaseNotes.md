# Release Notes

## 6.0.8-faithlife.2.22373.4

* Fix `IOException` in `ZipArchiveEntry.OpenInUpdateMode` when printing: [#6842](https://github.com/dotnet/wpf/issues/6842).

## 6.0.8-faithlife.1.22371.6

* Incorporate changes from [.NET 6.0.7](https://github.com/dotnet/wpf/compare/v6.0.6...v6.0.7).
* Fix TextBoxView memory leak for 2 seconds after unloading host control: [#1161](https://github.com/dotnet/wpf/pull/1161).
* Inline VerifyAccess: [#4021](https://github.com/dotnet/wpf/pull/4021).
* CommandParameter invalidates CanExecute: [#4217](https://github.com/dotnet/wpf/pull/4217).
* Harden events against race conditions: [#5722](https://github.com/dotnet/wpf/pull/5722).
* Fix ZeroForNow parameter: [#6657](https://github.com/dotnet/wpf/pull/6657).
* Fix MissingManifestResourceException when printing.

Thanks to contributors to this release: [@batzen](https://github.com/batzen), [Bruno Martinez](https://github.com/brunom), [@kant2002](https://github.com/kant2002), [@miloush](https://github.com/miloush), [@ThomasGoulet73](https://github.com/ThomasGoulet73).

## 6.0.7-faithlife.2.22317.5

* Fix packaging to repackage Microsoft.WindowsDesktop.App.Runtime.win-x64 v6.0.6 with the DLLs from this project.
* Reduce allocations when tracing routed events: [#6700](https://github.com/dotnet/wpf/pull/6700).

## 6.0.7-faithlife.1.22314.2

* Incorporate changes from [.NET 6.0.6](https://github.com/dotnet/wpf/compare/v6.0.5...v6.0.6).

## 6.0.6-faithlife.2.22313.3

* Use a stopwatch and timespan instead of DateTime and uint: [#1171](https://github.com/dotnet/wpf/pull/1171).
* Remove redundant static fields to reduce memory usage in XamlTypeInvoker: [#4027](https://github.com/dotnet/wpf/pull/4027).
* Remove unused local variable `node3Bounds` in `MS.Internal.Ink.StrokeNode.GetPointsAtMiddleSegment`: [#4256](https://github.com/dotnet/wpf/pull/4256).
* Replace Dictionary ContainsKey-Add with TryAdd: [#4486](https://github.com/dotnet/wpf/pull/4486).
* Remove unnecessary calculation in ImageSource.cs: [#5295](https://github.com/dotnet/wpf/pull/5295).
* Merge pattern in DispatcherOperation: [#5296](https://github.com/dotnet/wpf/pull/5296).
* Explicit delegate types: [#5954](https://github.com/dotnet/wpf/pull/5954).
* Remove unused files: [#6130](https://github.com/dotnet/wpf/pull/6130).
* Disable Indeterminate animation when hiding ProgressBar: [#6266](https://github.com/dotnet/wpf/pull/6266).
* Avoid excessive calls to the PropertyValues index getter: [#6293](https://github.com/dotnet/wpf/pull/6293).
* Account for optional out parameters in IStream: [#6345](https://github.com/dotnet/wpf/pull/6345).

Thanks to contributors to this release: [@batzen](https://github.com/batzen), [@kant2002](https://github.com/kant2002), [@lindexi](https://github.com/lindexi), [@miloush](https://github.com/miloush), [@paulozemek](https://github.com/paulozemek), [@ThomasGoulet73](https://github.com/ThomasGoulet73).

## 6.0.6-faithlife.1.22304.12

* Remove the custom HashSet class: [#3738](https://github.com/dotnet/wpf/pull/3738).
* Small performance improvement of PathParser: [#4208](https://github.com/dotnet/wpf/pull/4208).
* Use char overload in `string.Split`: [#4231](https://github.com/dotnet/wpf/pull/4231).
* Fix creating BitmapDecoder with an asynchronous file stream: [#4966](https://github.com/dotnet/wpf/pull/4966).
* Use `Clone` method to fast clone the array in StylusPoint: [#5218](https://github.com/dotnet/wpf/pull/5218).
* Optimize the code of OSVersionHelper: [#6252](https://github.com/dotnet/wpf/pull/6252).
* Eliminate memory copy when reading font data: [#6254](https://github.com/dotnet/wpf/pull/6254).
* Avoid unnecessary enumerator allocations in XamlDirective.GetHashCode [#6265](https://github.com/dotnet/wpf/pull/6265).
* Avoid exceptional string allocation in StaticExtension.ProvideValue: [#6269](https://github.com/dotnet/wpf/pull/6269).
* Don't allocate fallback name in XamlNamespace.GetXamlType unless it's needed: [#6270](https://github.com/dotnet/wpf/pull/6270).
* Remove substring allocation from Baml2006Reader.Logic_GetFullXmlns: [#6271](https://github.com/dotnet/wpf/pull/6271).
* Use span slice instead of substring in AbbreviatedGeometryParser.ReadNumber: [#6272](https://github.com/dotnet/wpf/pull/6272).
* Avoid boxing list enumerator in XamlObjectWriter.Logic_ConvertPositionalParamsToArgs:
[#6279](https://github.com/dotnet/wpf/pull/6279).
* Some improvements to FrugalList: [#6280](https://github.com/dotnet/wpf/pull/6280).
* Avoid boxing list/array enumerator in CreateTextLSRuns: [#6281](https://github.com/dotnet/wpf/pull/6281).
* Avoid enumerator boxing in XamlSchemaContext.UpdateNamespaceByUriList: [#6282](https://github.com/dotnet/wpf/pull/6282).
* Change most non-generic sorts to be generic: [#6285](https://github.com/dotnet/wpf/pull/6285).
* Stop boxing in Visual.SetDpiScaleVisualFlags: [#6309](https://github.com/dotnet/wpf/pull/6309).
* Remove closure/delegate allocation in ItemContainerGenerator: [#6396](https://github.com/dotnet/wpf/pull/6396).
* Avoid Hashtable-related allocations in AccessorTable: [#6500](https://github.com/dotnet/wpf/pull/6500).
* Avoid Hashtable-related allocations in DataBindEngine: [#6501](https://github.com/dotnet/wpf/pull/6501).
* Stop boxing WeakReferenceListEnumerator in PresentationSource use: [#6502](https://github.com/dotnet/wpf/pull/6502).
* Stop allocating unnecessary StringBuilders in ParsePropertyComments: [#6508](https://github.com/dotnet/wpf/pull/6508).
* Avoid unnecessary StringBuilder reallocation in LookupAndSetLocalizabilityAttribute: [#6509](https://github.com/dotnet/wpf/pull/6509).
* Avoid delegate allocation to call ListCollectionView.PrepareComparer: [#6511](https://github.com/dotnet/wpf/pull/6511).
* Avoid unnecessary List<> wrapper in GetTextRunSpans: [#6516](https://github.com/dotnet/wpf/pull/6516).
* Avoid unnecessary Collection<T> wrapper in CombineSources: [#6517](https://github.com/dotnet/wpf/pull/6517).
* Avoid allocating Stack<BranchNode> just to peek at it: [#6518](https://github.com/dotnet/wpf/pull/6518).
* Eliminate allocation in `StreamAsIStream.Read` [#6632](https://github.com/dotnet/wpf/pull/6632).

Thanks to contributors to this release: [@bgrainger](https://github.com/bgrainger), [@lindexi](https://github.com/lindexi), [@stephentoub](https://github.com/stephentoub), [@ThomasGoulet73](https://github.com/ThomasGoulet73).
