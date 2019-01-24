---
title: IDebugModule2::GetInfo | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugModule2::GetInfo
helpviewer_keywords:
- GetInfo method
- IDebugModule2::GetInfo method
ms.assetid: de337e66-294f-4ac9-b21e-71fac7418e36
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 476ffb2901dfe6a8d09ca707fc47089f4d99d97d
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54785247"
---
# <a name="idebugmodule2getinfo"></a>IDebugModule2::GetInfo
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu modül hakkında bilgi alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetInfo(   
   MODULE_INFO_FIELDS dwFields,  
   MODULE_INFO*       pInfo  
);  
```  
  
```cpp#  
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
