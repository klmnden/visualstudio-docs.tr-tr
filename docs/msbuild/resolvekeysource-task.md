---
title: ResolveKeySource görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#ResolveKeySource
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- ResolveKeySource task [MSBuild]
- MSBuild, ResolveKeySource task
ms.assetid: 449f06c2-e9aa-4236-ab1e-c45c25452b2e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 725e5816d6ea3f8323c9b1795faccef157ca9639
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54917074"
---
# <a name="resolvekeysource-task"></a>ResolveKeySource görevi
Tanımlayıcı ad anahtar kaynağını belirler.  
  
## <a name="task-parameters"></a>Görev parametreleri  
 Parametreleri aşağıdaki tabloda açıklanmıştır `ResolveKeySource` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`AutoClosePasswordPromptShow`|İsteğe bağlı `Int32` parametresi.<br /><br /> Alır veya ileti sayımın görüntülemek için saniye cinsinden süreyi ayarlar.|  
|`AutoClosePasswordPromptTimeout`|İsteğe bağlı `Int32` parametresi.<br /><br /> Alır veya parola istemi iletişim kutusunu kapatmadan önce beklenecek saniye cinsinden süreyi ayarlar.|  
|`CertificateFile`|İsteğe bağlı `String` parametresi.<br /><br /> Alır veya sertifika dosyasının yolunu ayarlar.|  
|`CertificateThumbprint`|İsteğe bağlı `String` parametresi.<br /><br /> Alır veya sertifika parmak izini ayarlar.|  
|`KeyFile`|İsteğe bağlı `String` parametresi.<br /><br /> Alır veya ayarlar anahtar dosyasının yolu.|  
|`ResolvedKeyContainer`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Alır veya ayarlar çözümlenen anahtar kapsayıcısı.|  
|`ResolvedKeyFile`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Alır veya ayarlar çözümlenen anahtar dosyası.|  
|`ResolvedThumbprint`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Alır veya çözümlenen sertifika parmak izini ayarlar.|  
|`ShowImportDialogDespitePreviousFailures`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`, önceki arızalarına Al iletişim kutusunu göster.|  
|`SuppressAutoClosePasswordPrompt`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Alır veya ayarlar parola istemi iletişim otomatik-kapatmaz olmadığını belirten bir Boole değeri.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)