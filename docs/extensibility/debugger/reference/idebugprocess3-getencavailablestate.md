---
title: IDebugProcess3::GetENCAvailableState | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProcess3::GetENCAvailableState
helpviewer_keywords:
- IDebugProcess3::GetENCAvailableState
ms.assetid: 98a5d527-8a72-476c-8e92-0bff3d97c195
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0ca55d7432ed921ef70b652cb92ce69f0d7e66cf
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54985100"
---
# <a name="idebugprocess3getencavailablestate"></a>IDebugProcess3::GetENCAvailableState
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