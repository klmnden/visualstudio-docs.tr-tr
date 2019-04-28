---
title: VCToolTask sınıfı | Microsoft Docs
ms.date: 03/10/2019
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
author: mikeblome
ms.author: mblome
ms.workload:
- multiple
ms.openlocfilehash: 7bdad856a6ea0ec6cca8292bc3095f51c500bcb1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62970724"
---
# <a name="vctooltask-base-class"></a>VCToolTask taban sınıfı

Birçok görevi sonuçta devralınacak <xref:Microsoft.Build.Utilities.Task> sınıfı ve [ToolTask](/dotnet/api/microsoft.build.utilities.tooltask) sınıfı. Bu sınıf, bunlardan türeyen görevlere birkaç parametre ekler. Bu parametreler, bu belgede listelenir.

## <a name="parameters"></a>Parametreler

Parametreleri aşağıdaki tabloda açıklanmıştır **VCToolTask** temel sınıfı.

|Parametre|Açıklama|
|---------------|-----------------|
|**ActiveToolSwitchesValues**|İsteğe bağlı **sözlük\<dize, ToolSwitch >** parametresi.|
|**AdditionalOptions**|İsteğe bağlı **dize** parametresi.|
|**EffectiveWorkingDirectory**|İsteğe bağlı **dize** parametresi.|
|**EnableErrorListRegex**|İsteğe bağlı **bool** parametresi.<br/><br/>Varsayılan değer `true`.|
|**ErrorListRegex**|İsteğe bağlı **Itaskıtem []** parametresi.|
|**ErrorListListExclusion**|İsteğe bağlı **Itaskıtem []** parametresi.|
|**GenerateCommandLine**|İsteğe bağlı **dize** parametresi.<br/><br/>Değerleri kullanan **CommandLineFormat** *biçimi* [varsayılan CommandLineFormat.ForBuildLog =] ve **EscapeFormat** *escapeFormat* [ Varsayılan EscapeFormat.Default =].|
|**GenerateCommandLineExceptSwitches**|İsteğe bağlı **dize** parametresi.<br/><br/>Değerleri kullanan **string []** *switchesToRemove*, **CommandLineFormat** *biçimi* [varsayılan CommandLineFormat.ForBuildLog =], ve **EscapeFormat** *escapeFormat* [varsayılan EscapeFormat.Default =].|

## <a name="see-also"></a>Ayrıca bkz.

[Görev başvurusu](../msbuild/msbuild-task-reference.md)<br/>
[Görevler](../msbuild/msbuild-tasks.md)