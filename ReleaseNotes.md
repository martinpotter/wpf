# Release Notes

## 6.1.0

* Optimize the code of OSVersionHelper: [#6252](https://github.com/dotnet/wpf/pull/6252).
* Eliminate memory copy when reading font data: [#6254](https://github.com/dotnet/wpf/pull/6254).
* Remove substring allocation from Baml2006Reader.Logic_GetFullXmlns: [#6271](https://github.com/dotnet/wpf/pull/6271).
* Remove some unnecessary StringBuilders: [#6275](https://github.com/dotnet/wpf/pull/6275).
* Change most non-generic sorts to be generic: [#6285](https://github.com/dotnet/wpf/pull/6285).
* Avoid Hashtable-related allocations in AccessorTable: [#6500](https://github.com/dotnet/wpf/pull/6500).
* Avoid Hashtable-related allocations in DataBindEngine: [#6501](https://github.com/dotnet/wpf/pull/6501).
* Stop boxing WeakReferenceListEnumerator in PresentationSource use: [#6502](https://github.com/dotnet/wpf/pull/6502).
* Stop allocating unnecessary StringBuilders in ParsePropertyComments: [#6508](https://github.com/dotnet/wpf/pull/6508).
* Avoid unnecessary StringBuilder reallocation in LookupAndSetLocalizabilityAttribute: [#6509](https://github.com/dotnet/wpf/pull/6509).
* Avoid delegate allocation to call ListCollectionView.PrepareComparer: [#6511](https://github.com/dotnet/wpf/pull/6511).
* Avoid unnecessary List<> wrapper in GetTextRunSpans: [#6516](https://github.com/dotnet/wpf/pull/6516).
* Avoid unnecessary Collection<T> wrapper in CombineSources: [#6517](https://github.com/dotnet/wpf/pull/6517).
* Avoid allocating Stack<BranchNode> just to peek at it: [#6518](https://github.com/dotnet/wpf/pull/6518).

Thanks to contributors to this release: [@bgrainger](https://github.com/bgrainger), [@lindexi](https://github.com/lindexi), [@stephentoub](https://github.com/stephentoub).
