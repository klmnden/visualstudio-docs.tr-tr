---
title: XslTransformation görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, XslTransformation task
- XslTransformation task [MSBuild]
ms.assetid: 6f3a7d81-3ae3-4703-9a06-870b32b69d80
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 892ecb7f97be3d89a0f6e8104b0b55647a6fe63e
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54793138"
---
# <a name="xsltransformation-task"></a>XslTransformation Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Bir XML dönüşümleri bir XSLT kullanarak giriş veya XSLT ve çıktıları çıktı cihazına veya bir dosya için derlenmiş.  
  
## <a name="parameters"></a>Parametreler  
 Parametreleri aşağıdaki tabloda açıklanmıştır `XslTransformation` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`OutputPaths`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br /> XML dönüştürme için Çıkış dosyalarını belirtir.|  
|`Parameters`|İsteğe bağlı `String` parametresi.<br /><br /> XSLT giriş belgesi için parametreleri belirtir.|  
|`XmlContent`|İsteğe bağlı `String` parametresi.<br /><br /> XML Giriş bir dize olarak belirtir.|  
|`XmlInputPaths`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametresi.<br /><br /> XML giriş dosyalarını belirtir.|  
|`XslCompiledDllPath`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br /> Derlenmiş XSLT belirtir.|  
|`XslContent`|İsteğe bağlı `String` parametresi.<br /><br /> XSLT Giriş bir dize olarak belirtir.|  
|`XslInputPath`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br /> XSLT giriş dosyasını belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Tabloda listelenen parametreleri sahip olmaya ek olarak, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension temel sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev Başvurusu](../msbuild/msbuild-task-reference.md)
