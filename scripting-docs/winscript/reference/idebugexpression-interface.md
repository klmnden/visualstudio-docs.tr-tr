---
title: Idebugexpression arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugExpression interface
ms.assetid: 36c00ffb-7160-4c30-a2c9-c9d70c8213cd
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 589c231afbc149c4eeface784d3cdbd43c4e5e40
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58156352"
---
# <a name="idebugexpression-interface"></a>IDebugExpression Arabirimi
Zaman uyumsuz olarak değerlendirilen bir ifade temsil eder. Komut dosyası motorları, genellikle bu arabirimi uygulayın. Hata ayıklayıcı IDE, bu arabirim genellikle hemen yürütme penceresi etkinleştirin veya Gözcü penceresi için kullanır.  
  
> [!NOTE]
>  `IDebugExpression` Yalnızca bir yığın çerçevesinde arabirimi kullanılabilir.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IDebugExpression` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugExpression::Start](../../winscript/reference/idebugexpression-start.md)|İfadenin değerlendirilmesi başlar.|  
|[IDebugExpression::Abort](../../winscript/reference/idebugexpression-abort.md)|İfade durdurur.|  
|[IDebugExpression::QueryIsComplete](../../winscript/reference/idebugexpression-queryiscomplete.md)|İşlemi tam olup olmadığını belirler.|  
|[IDebugExpression::GetResultAsString](../../winscript/reference/idebugexpression-getresultasstring.md)|Dize ve işlemin dönüş değeri olarak ifade değerlendirmesinin sonucu döndürür.|  
|[IDebugExpression::GetResultAsDebugProperty](../../winscript/reference/idebugexpression-getresultasdebugproperty.md)|Hata ayıklama özelliği ve işlemin dönüş değeri olarak ifade değerlendirmesinin sonucu döndürür.|