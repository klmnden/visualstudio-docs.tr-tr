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
ms.author: Michael.Blome
ms.workload:
- multiple
ms.openlocfilehash: 4c7cc3490735dbd9ac43cd43555ec673cc3afccd
ms.sourcegitcommit: 4ffb7be5384ad566ce46538032bf8561754c61a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2019
ms.locfileid: "58071161"
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