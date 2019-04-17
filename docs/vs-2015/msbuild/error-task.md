---
title: Hata görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#Error
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- Error task [MSBuild]
- MSBuild, Error task
ms.assetid: e96a90ee-a8ae-4e5b-8ef2-b5cf5fedd8b2
caps.latest.revision: 23
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: b220d12b872a81cba5f46bd14fdebafaa58cf4a1
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59652884"
---
# <a name="error-task"></a>Hata Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir derleme durdurur ve değerlendirilen bir koşullu ifadeye göre bir hatayı günlüğe kaydeder.  
  
## <a name="parameters"></a>Parametreler  
 Parametreleri aşağıdaki tabloda açıklanmıştır `Error` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`Code`|İsteğe bağlı `String` parametresi.<br /><br /> Şu hata ile ilişkilendirilecek hata kodu.|  
|`File`|İsteğe bağlı `String` parametresi.<br /><br /> Hata içeren dosyanın adı. Hata görevi içeren dosyanın dosya adı sağlanmazsa, kullanılır.|  
|`HelpKeyword`|İsteğe bağlı `String` parametresi.<br /><br /> Şu hata ile ilişkilendirmek için Yardım anahtar sözcüğü.|  
|`Text`|İsteğe bağlı `String` parametresi.<br /><br /> Hata metni, [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] günlüğe `Condition` parametresi değerlendirilen `true`.|  
  
## <a name="remarks"></a>Açıklamalar  
 `Error` Görev sağlayan [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] projeler günlükçüler için hata metni vermek ve derleme yürütmeyi durdurma.  
  
 Varsa `Condition` parametresi değerlendirilen `true`derleme durdurulur ve bir hata günlüğe kaydedilir. Varsa bir `Condition` parametresi mevcut değil, hata günlüğe kaydedilir ve yapı yürütmeyi durdurur. Günlüğe kaydetme hakkında daha fazla bilgi için bkz. [derleme günlükleri alma](../msbuild/obtaining-build-logs-with-msbuild.md).  
  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension temel sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneği, tüm gerekli özellikleri ayarlayın doğrular. Bunlar ayarlanmazsa, projeye bir hata olayı oluşturur ve değerini günlüklerini `Text` parametresinin `Error` görev.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <Target Name="ValidateCommandLine">  
        <Error  
            Text=" The 0 property must be set on the command line."  
            Condition="'$(0)' == ''" />  
        <Error  
            Text="The FREEBUILD property must be set on the command line."  
            Condition="'$(FREEBUILD)' == ''" />  
    </Target>  
    ...  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)   
 [Derleme Günlüklerini Alma](../msbuild/obtaining-build-logs-with-msbuild.md)
