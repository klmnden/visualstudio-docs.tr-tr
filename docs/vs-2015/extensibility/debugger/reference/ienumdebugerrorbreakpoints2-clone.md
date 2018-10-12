---
title: IEnumDebugErrorBreakpoints2::Clone | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IEnumDebugErrorBreakpoints2::Clone
helpviewer_keywords:
- IEnumDebugErrorBreakpoints2::Clone
ms.assetid: f6fb4985-8dd6-4a9b-98e0-15dbc64cc9ec
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 2feeddd66cd5f181d6ac838eb5630d4d79b01838
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49172425"
---
# <a name="ienumdebugerrorbreakpoints2clone"></a>IEnumDebugErrorBreakpoints2::Clone
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir kopyasını ayrı bir nesne olarak geçerli bir sabit listesi döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT Clone(  
   IEnumDebugErrorBreakpoints2** ppEnum  
);  
```  
  
```csharp  
int Clone(  
   out IEnumDebugErrorBreakpoints2 ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppEnum`  
 [out] Bu numaralandırma ayrı bir nesne gibi bir kopyasını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Numaralandırma kopyasını bu yöntemin çağrıldığı zaman orijinal ile aynı duruma sahiptir. Ancak, kopyanın ve orijinalin durumları ayrıdır ve ayrı ayrı değiştirilebilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IEnumDebugErrorBreakpoints2](../../../extensibility/debugger/reference/ienumdebugerrorbreakpoints2.md)

