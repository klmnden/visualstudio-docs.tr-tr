---
title: IDebugModule2::GetInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugModule2::GetInfo
helpviewer_keywords:
- GetInfo method
- IDebugModule2::GetInfo method
ms.assetid: de337e66-294f-4ac9-b21e-71fac7418e36
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c8b35cb0d77f2e078cf8a66ae095a939e361fd46
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55007873"
---
# <a name="idebugmodule2getinfo"></a>IDebugModule2::GetInfo
Bu modül hakkında bilgi alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetInfo(   
   MODULE_INFO_FIELDS dwFields,  
   MODULE_INFO*       pInfo  
);  
```  
  
```cpp  
int GetInfo(   
   enum_MODULE_INFO_FIELDS dwFields,  
   MODULE_INFO[]           pInfo  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwFields`  
 [in] Bayraklarının bir birleşimi [MODULE_INFO_FIELDS](../../../extensibility/debugger/reference/module-info-fields.md) hangi alanları belirten numaralandırma `pInfo` doldurulması için.  
  
 `pInfo`  
 [out içinde] A [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md) modül açıklaması ile doldurulmuş yapısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md) yapısı görüntülenen modülünün adı içeren **modülleri** penceresi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md)   
 [MODULE_INFO_FIELDS](../../../extensibility/debugger/reference/module-info-fields.md)   
 [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md)