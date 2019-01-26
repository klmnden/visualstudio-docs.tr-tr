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
ms.openlocfilehash: 59dd767e36620deb30d3d5ccff361d989c9d3a4d
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54928782"
---
# <a name="formatversion-task"></a>FormatVersion görevi
Düzeltme numarası için sürüm numarası ekler.  
  
-   #1. durum: Giriş: Sürüm =\<tanımlanmamış >;  Gözden geçirme =\<umursamaz >;   Çıkış: OutputVersion "1.0.0.0" =  
  
-   #2. durum: Giriş: Version="1.0.0.*"  Revision="5"  Output: OutputVersion="1.0.0.5"  
  
-   #3. durum: Giriş: Sürüm = "1.0.0.0" Düzeltme =\<umursamaz >;  Çıkış: OutputVersion "1.0.0.0" =  
  
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
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)