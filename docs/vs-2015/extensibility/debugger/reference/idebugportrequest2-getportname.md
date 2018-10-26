---
title: IDebugPortRequest2::GetPortName | Microsoft Docs
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
- IDebugPortRequest2::GetPortName
helpviewer_keywords:
- IDebugPortRequest2::GetPortName
ms.assetid: 53e2a3a4-bb34-4a02-a983-6bd84ea70587
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 047cd8e9643f976e78b49f7636b5daa156ad7d60
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49837158"
---
# <a name="idebugportrequest2getportname"></a>IDebugPortRequest2::GetPortName
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bağlantı noktası adını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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

