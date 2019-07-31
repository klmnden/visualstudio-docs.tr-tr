---
title: İleti görevi | Microsoft Docs
ms.date: 11/04/2016
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
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5efcc41a82cab32172aa395b488535f2777b9e13
ms.sourcegitcommit: 5694c5236fa32ba7f5bc1236a853f725ec7557e9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/31/2019
ms.locfileid: "68681165"
---
# <a name="message-task"></a>İleti görevi
Derleme sırasında bir iletiyi günlüğe kaydeder.

## <a name="parameters"></a>Parametreler
 Aşağıdaki tablo, `Message` görevin parametrelerini açıklar.

|Parametre|Açıklama|
|---------------|-----------------|
|`Importance`|İsteğe `String` bağlı parametre.<br /><br /> İletinin önemini belirtir. Bu parametre `high`, `normal` veya `low`değerine sahip olabilir. Varsayılan değer `normal` şeklindedir.|
|`Text`|İsteğe `String` bağlı parametre.<br /><br /> Günlüğe kaydedilecek hata metni.|

## <a name="remarks"></a>Açıklamalar
 Bu görev, projelerin, derleme işlemindeki farklı adımlarda oturum cihazlarına ileti vermesini sağlar [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)]. `Message`

 Parametresi olarak `true` değerlendirilirse`Text` , parametrenin değeri günlüğe kaydedilir ve derleme yürütülmeye devam eder. `Condition` Bir `Condition` parametre yoksa, ileti metni günlüğe kaydedilir. Günlüğe kaydetme hakkında daha fazla bilgi için bkz. [Derleme günlüklerini alma](../msbuild/obtaining-build-logs-with-msbuild.md).

 Varsayılan olarak, ileti MSBuild konsol günlükçüsü öğesine gönderilir. Bu, <xref:Microsoft.Build.Tasks.TaskExtension.Log%2A> parametresi ayarlanarak değiştirilebilir. Günlükçü, `Importance` parametreyi yorumlar. Genellikle, günlükçü ayrıntı düzeyi veya `high` üzeri olarak <xref:Microsoft.Build.Framework.LoggerVerbosity> `Minimal` ayarlandığında, olarak ayarlanmış bir ileti gönderilir. Günlükçü ayrıntı düzeyi olarak `low` <xref:Microsoft.Build.Framework.LoggerVerbosity> `Detailed`ayarlandığında, olarak ayarlanmış bir ileti gönderilir.

 Yukarıda listelenen parametrelere ek olarak, bu görev sınıfından devralınan <xref:Microsoft.Build.Tasks.TaskExtension> <xref:Microsoft.Build.Utilities.Task> parametreleri devralır. Bu ek parametrelerin ve açıklamalarının listesi için bkz. [TaskExtension temel sınıfı](../msbuild/taskextension-base-class.md).

## <a name="example"></a>Örnek
 Aşağıdaki kod örneği, tüm kayıtlı Günlükçüler için iletileri günlüğe kaydeder.

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
    <Target Name="DisplayMessages">
        <Message Text="Project File Name = $(MSBuildProjectFile)" />
        <Message Text="Project Extension = $(MSBuildProjectExtension)" />
    </Target>
    ...
</Project>
```

## <a name="see-also"></a>Ayrıca bkz.
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
- [Derleme günlüklerini al](../msbuild/obtaining-build-logs-with-msbuild.md)