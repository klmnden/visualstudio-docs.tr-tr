---
title: UpdateManifest görevi | Microsoft Docs
ms.date: 11/04/2016
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
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0dd2ddfdbe784a45badfd0138b41b1f5dbff8ec7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62954472"
---
# <a name="updatemanifest-task"></a>UpdateManifest görevi
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
 Tabloda listelenen parametreleri sahip olmaya ek olarak, bu görev parametreleri devralan <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [görev taban sınıfı](../msbuild/task-base-class.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Görevler](../msbuild/msbuild-tasks.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)