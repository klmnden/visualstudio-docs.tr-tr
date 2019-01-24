---
title: İleti görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#Message
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, Message task
- Message task [MSBuild]
ms.assetid: 2293309d-42b6-46dc-9684-8c146f66bc28
caps.latest.revision: 27
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 254602005966a9d9f95ff6b76f8ad42360e4a57d
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54770795"
---
# <a name="message-task"></a>İleti Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Derleme sırasında bir ileti kaydeder.  
  
## <a name="parameters"></a>Parametreler  
 Parametreleri aşağıdaki tabloda açıklanmıştır `Message` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`Importance`|İsteğe bağlı `String` parametresi.<br /><br /> İletinin önemini belirtir. Bu parametre değerini alabilir `high`, `normal` veya `low`. Varsayılan değer `normal` şeklindedir.|  
|`Text`|İsteğe bağlı `String` parametresi.<br /><br /> Oturum hata metni.|  
  
## <a name="remarks"></a>Açıklamalar  
 `Message` Görev sağlayan [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] projeleri günlükçüleri farklı derleme işlemindeki adımları sırasında sorun iletileri.  
  
 Varsa `Condition` parametresi değerlendirilen `true`, değerini `Text` parametresi kaydedilir ve yapı yürütülmeye devam eder. Varsa bir `Condition` parametresi mevcut değil, ileti metnini günlüğe kaydedilir. Günlüğe kaydetme hakkında daha fazla bilgi için bkz. [derleme günlükleri alma](../msbuild/obtaining-build-logs-with-msbuild.md).  
  
 Varsayılan olarak MSBuild konsol Oluşturucusu'na ileti gönderilir. Bu ayarı değiştirilebilir <xref:Microsoft.Build.Tasks.TaskExtension.Log%2A> parametresi. Günlükçü yorumlar `Importance` parametresi.  
  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension temel sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneği, tüm kayıtlı günlükçüler için iletileri günlüğe kaydeder.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <Target Name="DisplayMessages">  
        <Message Text="Project File Name = $(MSBuildProjectFile)" />  
        <Message Text="Project Extension = $(MSBuildProjectExtension)" />  
    </Target>  
    ...  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)   
 [Derleme Günlüklerini Alma](../msbuild/obtaining-build-logs-with-msbuild.md)
