---
Description: ShareTarget
MS-HAID: AppxManifestSchema2010\_v2.element\_ShareTarget
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/apps
Search.Product: eADQiWindows 10XVcnh
title: ShareTarget
ms.assetid: 42f77354-83be-4f41-bf89-95566d026687
author: laurenhughes
ms.author: lahugh
keywords: windows 10, uwp, schema, package manifest
---

# ShareTarget




Declares an app extension point of type **windows.shareTarget**. The app can share the specified types of files.

## Element hierarchy

<dl>
<dt><a href="element-extension.md">&lt;Extension&gt;</a></dt>
<dd><b>&lt;ShareTarget&gt;</b></dd>
</dl>

## Syntax

``` syntax
<ShareTarget m:Description? = A string between 1 and 255 characters in length. >

  <!-- Child elements -->
  SupportedFileTypes?,
  DataFormat{0,10000}

</ShareTarget>
```

### Key

`?`   optional (zero or one)
`{}`   specific range of occurrences
## Attributes and Elements


### Attributes

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribute</th>
<th>Description</th>
<th>Data type</th>
<th>Required</th>
<th>Default value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>m:Description</strong></td>
<td><p>The description of the shared target. This string is localizable. </p></td>
<td>A string between 1 and 255 characters in length.</td>
<td>No</td>
<td></td>
</tr>
</tbody>
</table>

 

### Child Elements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Child Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>[DataFormat](element-dataformat.md)</td>
<td><p>Specifies a data package format such as text or HTML format that the app can share. It is unique per application in the package and is case sensitive.</p></td>
</tr>
<tr class="even">
<td>[SupportedFileTypes (type: CT_CharmsSupportedFileTypes)](element-1-supportedfiletypes.md)</td>
<td><p>Defines the file types that the app can share.</p></td>
</tr>
</tbody>
</table>

 

### Parent Elements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parent Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>[Extension (type: CT_ApplicationExtension)](element-extension.md)</td>
<td><p>Declares an extensibility point for the app.</p></td>
</tr>
</tbody>
</table>

 

## Remarks

The Share charm provides access to a list of target apps that can receive data that the user wants to share. This extensibility point enables your app to be included in the list of share targets.

**ShareTarget** must specify either [**SupportedFileTypes**](element-1-supportedfiletypes.md) element, or at least one [**DataFormat**](element-dataformat.md) element. It can't omit both. The schema allows omitting both, but semantic validation will fail.

## Examples

```XML
<Extension Category="windows.shareTarget">
  <ShareTarget>
    <SupportedFileTypes>
      <SupportsAnyFileType />
    </SupportedFileTypes>
    <DataFormat>Text</DataFormat>
    <DataFormat>Uri</DataFormat>
    <DataFormat>Bitmap</DataFormat>
    <DataFormat>Html</DataFormat>
    <DataFormat>http://schema.org/Book</DataFormat>
  </ShareTarget>
</Extension>
```

## See also


**Tasks**
[Adding share](https://msdn.microsoft.com/library/windows/apps/hh758314)

**Concepts**
[App contracts and extensions](https://msdn.microsoft.com/library/windows/apps/hh464906)

## Requirements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>http://schemas.microsoft.com/appx/2010/manifest</p></td>
</tr>
</tbody>
</table>

 

 


