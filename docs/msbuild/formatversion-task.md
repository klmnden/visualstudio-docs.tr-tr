---
title: FormatVersion görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
ms.assetid: 96e692f6-b581-46ca-8cc9-441a1861e371
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 67cdd6fa3517402dbd9c1e85a84f762f9aa7dd17
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60058155"
---
# <a name="formatversion-task"></a>FormatVersion görevi
Düzeltme numarası için sürüm numarası ekler.

- #1. durum: Giriş: Sürüm =\<tanımlanmamış >;  Gözden geçirme =\<umursamaz >;   Çıkış: OutputVersion "1.0.0.0" =

- #2. durum: Giriş: Version="1.0.0.*"  Revision="5"  Output: OutputVersion="1.0.0.5"

- #3. durum: Giriş: Sürüm = "1.0.0.0" Düzeltme =\<umursamaz >;  Çıkış: OutputVersion "1.0.0.0" =

## <a name="parameters"></a>Parametreler
 Parametreleri aşağıdaki tabloda açıklanmıştır `FormatVersion` görev.

|Parametre|Açıklama|
|---------------|-----------------|
|`FormatType`|İsteğe bağlı `String` parametresi.<br /><br /> Biçim türünü belirtir.<br /><br /> -"Sürüm" = sürümü.<br />-"Path"= Değiştir"." ile "_";|
|`OutputVersion`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Düzeltme numarası içeren çıkış sürümünü belirtir.|
|`Revision`|İsteğe bağlı `Int32` parametresi.<br /><br /> Düzeltme sürümü eklenecek belirtir.|
|`Version`|İsteğe bağlı `String` parametresi.<br /><br /> Sürüm numarası dizeyi biçimlendirmek için belirtir.|

## <a name="remarks"></a>Açıklamalar
 Tabloda listelenen parametreleri sahip olmaya ek olarak, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Görevler](../msbuild/msbuild-tasks.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)