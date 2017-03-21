---
author: laurenhughes
ms.assetid: 4aaee0da-1eff-4a8f-972e-0f8706ab2ca0
title: com:Version (in Package/Extensions)
description: Version number and additional information about the type library.
ms.author: lahugh
ms.date: 03/29/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp, schema, manifest, com
---


# com:Version (in Package/Extensions)

## -description
Version number and additional information about the type library.

## -element-hierarchy
<dl>
<dt><a href="element-package.md">&lt;Package&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-extensions.md">&lt;Extensions&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-extension.md">&lt;Extension&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-com-package-cominterface.md">&lt;ComInterface&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-com-package-typelib.md">&lt;TypeLib&gt;</a></dt>
<dd><b>&lt;Version&gt;</b></dd>
</dl>
</dd>
</dl>
</dd>
</dl>
</dd>
</dl>
</dd>
</dl>



## -syntax
```syntax
<Version
    VersionNumber = One to three alphanumeric characters separated by a period followed by one to three more alphanumeric characters, e.g., 1.5a
    LocaleId? = A string in hexadecimal format containing numbers or the letters a, b, c, d, e, f (capital or lower case).
    LibraryFlag? = An integer value in the range of 0 to 15.
    HelpDirectory? = A string between 1 and 32767 characters in length with a non-whitespace character at its beginning and end. >

  <!-- Child elements -->
  ( Win32Path,
    Win64Path )  
</Version>
```

## -key
`?`    optional (zero or one) 

## -attributes

| Attribute | Description | Data type | Required |
|-----------|-------------|-----------|----------|
| VersionNumber | The name of the version number. | One to three alphanumeric characters separated by a period followed by one to three more alphanumeric characters, e.g., 1.5a | Yes |
| LocaleId | An Id representing geographic location. | A string in hexadecimal format containing numbers or the letters a, b, c, d, e, f (capital or lower case). | No |
| LibraryFlag | An integer value from the [LIBFLAGS](https://msdn.microsoft.com/library/windows/desktop/ms221149.aspx) enumeration. | An integer value in the range of 0 to 15. | No |
| HelpDirectory | The HELPDIR subkey. | A string between 1 and 32767 characters in length with a non-whitespace character at its beginning and end. | No |

## -child-elements
 
| Child Element | Description |
|---------------|-------------|
| [Win32Path](element-com-package-win32path.md) | A path to the 32-bit type library. |
| [Win64Path](element-com-package-win64path.md) | A path to the 64-bit type library. |

## -remarks
For more information about type libraries and the attributes on this page, see [Registering a Type Library](https://msdn.microsoft.com/library/windows/desktop/ms221610.aspx).

> [!NOTE]  
> You must specify both a Win32Path and a Win64Path. 

## -examples

## -requirements
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>http://schemas.microsoft.com/appx/manifest/com/windows10</p></td>
</tr>
</tbody>
</table>