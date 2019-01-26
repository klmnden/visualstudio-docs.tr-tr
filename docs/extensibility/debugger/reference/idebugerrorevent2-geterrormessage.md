---
title: IDebugErrorEvent2::GetErrorMessage | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugErrorEvent2::GetErrorMessage
helpviewer_keywords:
- IDebugErrorEvent2::GetErrorMessage
ms.assetid: 9e3b0d74-a2dd-4eaa-bd95-21b2f9c79409
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 70dc659fa1e3db2d4db797f3be82ba0239368f47
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/26/2019
ms.locfileid: "55069440"
---
# <a name="idebugerrorevent2geterrormessage"></a>IDebugErrorEvent2::GetErrorMessage
Kullanıcı tarafından okunabilen bir ileti yapımı sağlayan bilgileri döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetErrorMessage(  
   MESSAGETYPE* pMessageType,  
   BSTR*        pbstrErrorFormat,  
   HRESULT*     hrErrorReason,  
   DWORD*       pdwType,  
   BSTR*        pbstrHelpFileName,  
   DWORD*       pdwHelpId  
);  
```  
  
```csharp  
int GetErrorMessage(  
   out enum_MESSAGETYPE   pMessageType,  
   out string             pbstrErrorFormat,  
   out int                phrErrorReason,  
   out uint               pdwType,  
   out string             pbstrHelpFileName,  
   out uint               pdwHelpId  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pMessageType`  
 [out] Bir değer döndürür [MESSAGETYPE](../../../extensibility/debugger/reference/messagetype.md) ileti tipini açıklayan sabit listesi,.  
  
 `pbstrErrorFormat`  
 [out] Kullanıcı için son ileti biçimi (Ayrıntılar için bkz: "Açıklamalar").  
  
 `hrErrorReason`  
 [out] Hata iletisi hakkında kodudur.  
  
 `pdwType`  
 [out] Hata önem derecesi (için MB_XXX sabitleri kullanın `MessageBox`; Örneğin, `MB_EXCLAMATION` veya `MB_WARNING`).  
  
 `pbstrHelpFileName`  
 [out] Yardım dosyası (Yardım dosyası yoksa null bir değere ayarlanmış) yolu.  
  
 `pdwHelpId`  
 [out] (Yardım konusu yok ise 0 olarak ayarlanırsa) görüntülemek için Yardım konusu kimliği.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Hata iletisi satırlar boyunca biçimlendirilmelidir `"What I was doing.  %1"`. `"%1"` Sonra çağıran tarafından türetilmiş hata kodundan hata iletisiyle geçecekti (içinde döndürülen `hrErrorReason`). `pMessageType` Parametresi arayan nasıl son hata iletisinin gösterilmemesi gerektiğini bildirir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugErrorEvent2](../../../extensibility/debugger/reference/idebugerrorevent2.md)   
 [MESSAGETYPE](../../../extensibility/debugger/reference/messagetype.md)