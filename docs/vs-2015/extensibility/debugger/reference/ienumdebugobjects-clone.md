---
title: IEnumDebugObjects::Clone | Microsoft Docs
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
- IEnumDebugObjects::Clone
helpviewer_keywords:
- IEnumDebugObjects::Clone method
ms.assetid: cb7df109-d29a-4218-b900-6809091459dd
caps.latest.revision: 6
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 60a21d41c300a0b546294451b6913a1d6ee7c514
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49177612"
---
# <a name="ienumdebugobjectsclone"></a>IEnumDebugObjects::Clone
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem bir kopyasını ayrı bir nesne olarak geçerli bir sabit listesi döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT Clone(  
   IEnumDebugObjects** ppEnum  
);  
```  
  
```csharp  
int Clone(  
   out IEnumDebugObjects ppEnum  
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
 [IEnumDebugObjects](../../../extensibility/debugger/reference/ienumdebugobjects.md)

