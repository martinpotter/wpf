# Release Notes

## 6.1.0

* Remove the custom HashSet class: [#3738](https://github.com/dotnet/wpf/pull/3738).
* Small performance improvement of PathParser: [#4208](https://github.com/dotnet/wpf/pull/4208).
* Use char overload in `string.Split`: [#4231](https://github.com/dotnet/wpf/pull/4231).
* Fix creating BitmapDecoder with an asynchronous file stream: [#4966](https://github.com/dotnet/wpf/pull/4966).
* Use `Clone` method to fast clone the array in StylusPoint: [#5218](https://github.com/dotnet/wpf/pull/5218).
* Optimize the code of OSVersionHelper: [#6252](https://github.com/dotnet/wpf/pull/6252).
* Eliminate memory copy when reading font data: [#6254](https://github.com/dotnet/wpf/pull/6254).
* Avoid unnecessary enumerator allocations in XamlDirective.GetHashCode [#6265](https://github.com/dotnet/wpf/pull/6265).
* Avoid exceptional string allocation in StaticExtension.ProvideValue: [#6269](https://github.com/dotnet/wpf/pull/6269).
* Don't allocate fallback name in XamlNamespace.GetXamlType unless it's needed: [[#6270](https://github.com/dotnet/wpf/pull/6270).
* Remove substring allocation from Baml2006Reader.Logic_GetFullXmlns: [#6271](https://github.com/dotnet/wpf/pull/6271).
* Use span slice instead of substring in AbbreviatedGeometryParser.ReadNumber: [#6272](https://github.com/dotnet/wpf/pull/6272).
* Remove some unnecessary StringBuilders: [#6275](https://github.com/dotnet/wpf/pull/6275).
* Avoid boxing list enumerator in XamlObjectWriter.Logic_ConvertPositionalParamsToArgs:
[#6279](https://github.com/dotnet/wpf/pull/6279).
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

Thanks to contributors to this release: [@bgrainger](https://github.com/bgrainger), [@lindexi](https://github.com/lindexi), [@stephentoub](https://github.com/stephentoub), [@ThomasGoulet73](https://github.com/ThomasGoulet73).
