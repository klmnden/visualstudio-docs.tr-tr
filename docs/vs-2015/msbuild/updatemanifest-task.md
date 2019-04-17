---
title: UpdateManifest görevi | Microsoft Docs
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
- MSBuild, UpdateManifest task
- UpdateManifest task [MSBuild]
ms.assetid: 1291fd33-b89e-4e15-8fb1-69f9625cf2d2
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 5e2ec8a0cd854a04c338add22c3f90daf0bf14ba
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59657005"
---
# <a name="updatemanifest-task"></a>UpdateManifest Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir bildirimdeki seçili özelliklerini güncelleştirir ve Çekildi.  
  
## <a name="parameters"></a>Parametreler  
 Parametreleri aşağıdaki tabloda açıklanmıştır `UpdateManifest` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`ApplicationManifest`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br /> Uygulama bildirimini belirtir.|  
|`ApplicationPath`|Gerekli `String` parametresi.<br /><br /> Uygulama bildiriminin yolu belirtir.|  
|`InputManifest`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br /> Güncelleştirilecek bildirimini belirtir.|  
|`OutputManifest`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> çıkış parametresi.<br /><br /> Güncelleştirilmiş özellikleri içeren bildirimini belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Tabloda listelenen parametreleri sahip olmaya ek olarak, bu görev parametreleri devralan <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [görev temel sınıf](../msbuild/task-base-class.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev Başvurusu](../msbuild/msbuild-task-reference.md)
