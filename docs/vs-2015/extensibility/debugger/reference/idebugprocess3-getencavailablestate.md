---
title: IDebugProcess3::GetENCAvailableState | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProcess3::GetENCAvailableState
helpviewer_keywords:
- IDebugProcess3::GetENCAvailableState
ms.assetid: 98a5d527-8a72-476c-8e92-0bff3d97c195
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 17bf401b9992d156fdaba60ae46bffde6f8ce8cc
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54754433"
---
# <a name="idebugprocess3getencavailablestate"></a>IDebugProcess3::GetENCAvailableState
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem geçerli Düzenle ve devam et işleminin durumunu alır. Özel bağlantı noktası sağlayıcısı her zaman döndürmelidir `E_NOTIMPL`.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetENCAvailableState(  
   EncUnavailableReason* pReason  
);  
```  
  
```csharp  
int GetENCAvailableState(  
   EncUnavailableReason[] pReason  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pReason`  
 [out] Bir değer [EncUnavailableReason](../../../extensibility/debugger/reference/encunavailablereason.md) sabit listesi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.  
  
> [!NOTE]
>  Özel bağlantı noktası sağlayıcısı her zaman döndürmelidir `E_NOTIMPL`.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu durum etkilenebilir [DisableENC](../../../extensibility/debugger/reference/idebugprocess3-disableenc.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProcess3](../../../extensibility/debugger/reference/idebugprocess3.md)   
 [DisableENC](../../../extensibility/debugger/reference/idebugprocess3-disableenc.md)   
 [EncUnavailableReason](../../../extensibility/debugger/reference/encunavailablereason.md)
