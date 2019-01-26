---
title: IDebugPortRequest2::GetPortName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPortRequest2::GetPortName
helpviewer_keywords:
- IDebugPortRequest2::GetPortName
ms.assetid: 53e2a3a4-bb34-4a02-a983-6bd84ea70587
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: cd5033926987ef1a2673380a4f7d76dc1b0cb0c0
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54962738"
---
# <a name="idebugportrequest2getportname"></a>IDebugPortRequest2::GetPortName
Bağlantı noktası adını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetPortName(   
   BSTR* pbstrPortName  
);  
```  
  
```csharp  
int GetPortName(   
   out string pbstrPortName  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pbstrPortName`  
 [out] Bağlantı noktası adını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 [IDebugPortRequest2](../../../extensibility/debugger/reference/idebugportrequest2.md) arabirimi genellikle geçirilen bir hata ayıklama paketi (istemci) bir bağlantı almak için bir bağlantı noktası sağlayıcısı için (sunucu) için bir bağlantı noktası. Hata ayıklama paketi hem de bağlantı noktası sağlayıcısı bağlantı noktası için olası seçeneklerin farkındayız. Bağlantı noktası, basit bir dize tanımlayabilir, ardından `IDebugPortRequest2::GetPortName` yöntemi bağlantı kurmak için yeterli bilgi vardır. Aksi takdirde, ek arabirimleri sunucusu kullanılarak elde edilebilir istemci tarafından sağlanabilir `IDebugPortRequest2::QueryInterface`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPortRequest2](../../../extensibility/debugger/reference/idebugportrequest2.md)