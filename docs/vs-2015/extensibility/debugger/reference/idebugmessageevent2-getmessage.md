---
title: IDebugMessageEvent2::GetMessage | Microsoft Docs
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
- IDebugMessageEvent2::GetMessage
helpviewer_keywords:
- GetMessage method
- IDebugMessageEvent2::GetMessage method
ms.assetid: 9fca7285-f7f1-422d-8565-92bf0e0db60a
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 777c5e1198b26c7d4145736caad42c8a52e95d90
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49307644"
---
# <a name="idebugmessageevent2getmessage"></a>IDebugMessageEvent2::GetMessage
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Görüntülenecek iletiyi alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetMessage(   
   MESSAGETYPE* pMessageType,  
   BSTR*        pbstrMessage,  
   DWORD*       pdwType,  
   BSTR*        pbstrHelpFileName,  
   DWORD*       pdwHelpId  
);  
```  
  
```csharp  
int GetMessage(   
   out enum_MESSAGETYPE pMessageType,  
   out string           pbstrMessage,  
   out uint             pdwType,  
   out string           pbstrHelpFileName,  
   out uint             dwHelpId  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pMessageType`  
 [out] Bir değer döndürür [MESSAGETYPE](../../../extensibility/debugger/reference/messagetype.md) ileti türünü açıklayan sabit listesi.  
  
 `pbstrMessage`  
 [out] Bir ileti döndürür.  
  
 `pdwType`  
 [out] Win32 kuralları kullanılarak iletisinin türü döndürür `MessageBox` işlevi. Bkz: [AfxMessageBox](http://msdn.microsoft.com/library/d66d0328-cdcc-48f6-96a4-badf089099c8) Ayrıntılar için işlevi.  
  
 `pbstrHelpFileName`  
 [out içinde] Yardım dosyası adı döndürür. Yardım dosyası yoksa (C++) null veya boş (C#) değeri olabilir.  
  
 `pdwHelpId`  
 [out içinde] Yardım tanımlayıcısını döndürür. Yardım yoksa 0, bu iletiyle ilişkili.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugMessageEvent2](../../../extensibility/debugger/reference/idebugmessageevent2.md)   
 [MESSAGETYPE](../../../extensibility/debugger/reference/messagetype.md)   
 [AfxMessageBox](http://msdn.microsoft.com/library/d66d0328-cdcc-48f6-96a4-badf089099c8)

