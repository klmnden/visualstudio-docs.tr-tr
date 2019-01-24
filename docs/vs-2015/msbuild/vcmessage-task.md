---
title: VCMessage görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
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
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: e1011ccfe1609376dc496dc6eb8e7f50795fab5c
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54784505"
---
# <a name="vcmessage-task"></a>VCMessage Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Uyarı günlükleri ve bir yapı sırasında hata iletileri.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu görevi, MSBuild uygulamak için Visual C++ yardımcı olur ve kullanıcı tarafından çağrılması amaçlanmamıştır. Daha fazla bilgi için bkz. <xref:Microsoft.Build.Utilities.TaskLoggingHelper>.  
  
## <a name="parameters"></a>Parametreler  
 Parametreleri aşağıdaki tabloda açıklanmıştır **VCMessage** görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|**Bağımsız Değişkenler**|İsteğe bağlı **dize** parametresi.<br /><br /> Görüntülenecek iletiler noktalı virgülle ayrılmış listesi.|  
|**Kod**|Gerekli **dize** parametresi.<br /><br /> İleti niteleyen hata numarası.|  
|**Tür**|İsteğe bağlı **dize** parametresi.<br /><br /> Yaymak üzere ileti türünü belirtir. Seçeneklerinden birini belirtin `"Warning"` bir uyarı iletisi yaymak için veya `"Error"` bir hata iletisi yayılamıyor.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görev Başvurusu](../msbuild/msbuild-task-reference.md)
