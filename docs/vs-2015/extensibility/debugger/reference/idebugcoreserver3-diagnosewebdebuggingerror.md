---
title: IDebugCoreServer3::DiagnoseWebDebuggingError | Microsoft Docs
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
- IDebugCoreServer3::DiagnoseWebDebuggingError
helpviewer_keywords:
- IDebugCoreServer3::DiagnoseWebDebuggingError
ms.assetid: 8c4570ca-ae55-42f2-bbaa-8d8e75d2fa19
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: d9359637a4a1bbd1650a80c8210f615964703d68
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49907774"
---
# <a name="idebugcoreserver3diagnosewebdebuggingerror"></a>IDebugCoreServer3::DiagnoseWebDebuggingError
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir auto-attach neden belirleme girişimi başarısız oldu.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT DiagnoseWebDebuggingError(  
   LPCWSTR pszUrl  
);  
```  
  
```csharp  
int DiagnoseWebDebuggingError(  
   string pszUrl  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pszUrl`  
 [in] Şu anda kullanılmıyor; her zaman null değerine ayarlanmalıdır.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Tipik diğer dönüş kodları şunlardır:  
  
|Kod|Açıklama|  
|----------|-----------------|  
|`S_WEBDBG_UNABLE_TO_DIAGNOSE`|Hata ayıklamayı başlatmak uzak sunucu başarısız olmasının belirlenemiyor.|  
|`S_WEBDBG_DEBUG_VERB_BLOCKED`|Büyük olasılıkla yetersiz izinler nedeniyle uzak sunucuda hata ayıklaması yapılamıyor veya DEBUG fiilini etkin değil.|  
|`E_WEBDBG_DEBUG_VERB_BLOCKED`|Web sunucusu kilitlenmiş ve hata ayıklamayı etkinleştirmek için gerekli olan DEBUG fiilini engelliyor.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md)

