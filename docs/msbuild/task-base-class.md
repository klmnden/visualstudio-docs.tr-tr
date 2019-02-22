---
title: Görev taban sınıfı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
ms.assetid: 6c3f6238-b9f0-4325-b8b0-de61090bd0a2
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9662a504232c70662e40db54e3eda27aa4abe835
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56642969"
---
# <a name="task-base-class"></a>Görev taban sınıfı
Birçok görevi sonuçta devralınacak <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu sınıf, bunlardan türeyen görevlere birkaç parametre ekler. Bu parametreler, bu belgede listelenir.

## <a name="parameters"></a>Parametreler
 Aşağıdaki tabloda, bu temel sınıfın parametreler açıklanmıştır.

|Parametre|Açıklama|
|---------------|-----------------|
|<xref:Microsoft.Build.Utilities.Task.BuildEngine%2A>|İsteğe bağlı <xref:Microsoft.Build.Framework.IBuildEngine> parametresi.<br /><br /> Görevler için kullanılabilir derleme altyapısı arabirimi belirtir. Yapı altyapısının geri içine çağırmak görevlere izin vermek için bu parametreyi otomatik olarak ayarlar.|
|<xref:Microsoft.Build.Utilities.Task.BuildEngine2%2A>|İsteğe bağlı <xref:Microsoft.Build.Framework.IBuildEngine2> parametresi.<br /><br /> Görevler için kullanılabilir derleme altyapısı arabirimi belirtir. Yapı altyapısının geri içine çağırmak görevlere izin vermek için bu parametreyi otomatik olarak ayarlar.<br /><br /> Bu sınıftan devralmayı görev yazarları, değerinden dönüştürme gerekmez. böylece bu kullanışlı bir özelliktir `IBuildEngine` için `IBuildEngine2`.|
|<xref:Microsoft.Build.Utilities.Task.BuildEngine3%2A>|İsteğe bağlı <xref:Microsoft.Build.Framework.IBuildEngine3> parametresi.<br /><br /> Ana bilgisayar tarafından sağlanan yapı altyapısı arabirimi belirtir.|
|<xref:Microsoft.Build.Utilities.Task.HostObject%2A>|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskHost> parametresi.<br /><br /> (Null olabilir) konak nesne örneğini belirtir. Yapı altyapısının, IDE konak bir konak nesnesi bu belirli görev ile ilişkili varsa bu özelliği ayarlar.|
|<xref:Microsoft.Build.Utilities.Task.Log%2A>|İsteğe bağlı <xref:Microsoft.Build.Utilities.TaskLoggingHelper> salt okunur parametre.<br /><br /> Günlüğe kaydetme yardımcı nesnesi...|

## <a name="see-also"></a>Ayrıca bkz.
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
- [Görevler](../msbuild/msbuild-tasks.md)