---
title: VCMessage görevi | Microsoft Docs
ms.date: 06/27/2018
ms.topic: reference
f1_keywords:
- vc.task.vcmessage
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- VCMessage task (MSBuild (Visual C++))
- MSBuild (Visual C++), VCMessage task
ms.assetid: 956675fd-05dc-40b4-856f-616145103498
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d025fd1f71b67acbcd532232b36b55fd35e1f530
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56596067"
---
# <a name="vcmessage-task"></a>VCMessage görevi
Uyarı günlükleri ve bir yapı sırasında hata iletileri.

## <a name="remarks"></a>Açıklamalar
 Bu görevi, MSBuild uygulamak için Visual C++ yardımcı olur ve kullanıcı tarafından çağrılması amaçlanmamıştır. Daha fazla bilgi için bkz. <xref:Microsoft.Build.Utilities.TaskLoggingHelper>.

## <a name="parameters"></a>Parametreler
 Parametreleri aşağıdaki tabloda açıklanmıştır **VCMessage** görev.

|Parametre|Açıklama|
|---------------|-----------------|
|**Bağımsız Değişkenler**|İsteğe bağlı **dize** parametresi.<br /><br /> Görüntülenecek iletiler noktalı virgülle ayrılmış listesi.|
|**Kod**|Gerekli **dize** parametresi.<br /><br /> İleti niteleyen hata numarası.|
|**Tür**|İsteğe bağlı **dize** parametresi.<br /><br /> Yaymak üzere ileti türünü belirtir. "Uyarı" bir uyarı iletisi göstermek için oluşturabilir veya bir hata iletisi göstermek için "Error" belirtin.|

## <a name="see-also"></a>Ayrıca bkz.
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)