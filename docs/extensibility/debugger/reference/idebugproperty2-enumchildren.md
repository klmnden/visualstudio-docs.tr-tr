---
title: IDebugProperty2::EnumChildren | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProperty2::EnumChildren
helpviewer_keywords:
- IDebugProperty2::EnumChildren
ms.assetid: cf79f666-65d1-417c-af7c-9271bac9a267
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e6f297b4adf3c7194340bfdda71936de93c4506a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54988252"
---
# <a name="idebugproperty2enumchildren"></a>IDebugProperty2::EnumChildren
Alt özellik öğelerinin bir listesini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT EnumChildren (   
   DEBUGPROP_INFO_FLAGS      dwFields,  
   DWORD                     dwRadix,  
   REFGUID                   guidFilter,  
   DBG_ATTRIB_FLAGS          dwAttribFilter,  
   LPCOLESTR                 pszNameFilter,  
   DWORD                     dwTimeout,  
   IEnumDebugPropertyInfo2** ppEnum  
);  
```  
  
```csharp  
int EnumChildren (   
   enum_DEBUGPROP_INFO_FLAGS   dwFields,  
   uint                        dwRadix,  
   ref Guid                    guidFilter,  
   uint                        dwAttribFilter,  
   string                      pszNameFilter,  
   uint                        dwTimeout,  
   out IEnumDebugPropertyInfo2 ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwFields`  
 [in] Bayraklarının bir birleşimi [DEBUGPROP_INFO_FLAGS](../../../extensibility/debugger/reference/debugprop-info-flags.md) hangi alanların numaralandırılmış belirten numaralandırma [DEBUG_PROPERTY_INFO](../../../extensibility/debugger/reference/debug-property-info.md) yapılardır doldurulmalıdır.  
  
 `dwRadix`  
 [in] Sayısal yedeklenmesine biçimlendirmede kullanılacak sayı tabanı belirtir.  
  
 `guidFilter`  
 [in] GUID ile kullanılan filtrenin `dwAttribFilter` ve `pszNameFilter` hangi parametreleri `DEBUG_PROPERTY_INFO` alt öğesi olan sıralanması. Örneğin, `guidFilterLocals` yerel değişkenler için filtreler.  
  
 `dwAttribFilter`  
 [in] Bayraklarının bir birleşimi [DBG_ATTRIB_FLAGS](../../../extensibility/debugger/reference/dbg-attrib-flags.md) belirtir, örneğin Numaralandırılacak nesnelerin türü numaralandırması `DBG_ATTRIB_METHOD` alt öğeleri bu özelliğin olabilecek tüm yöntemleri için. Birlikte `guidFilter` ve `pszNameFilter` parametreleri.  
  
 `pszNameFilter`  
 [in] İle kullanılan filtresinin adını `guidFilter` ve `dwAttribFilter` hangi parametreleri `DEBUG_PROPERTY_INFO` alt öğesi olan sıralanması. Örneğin, bu parametre "MyX" filtreleri adı "MyX." tüm alt ayarlama  
  
 `dwTimeout`  
 [in] Bu yöntemden geri dönmeden önce beklenecek milisaniye cinsinden en uzun süreyi belirtir. Kullanım `INFINITE` süresiz bekleme.  
  
 `ppEnum`  
 [out] Döndürür bir [IEnumDebugPropertyInfo2](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2.md) alt özellikleri listesini içeren nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)   
 [DEBUGPROP_INFO_FLAGS](../../../extensibility/debugger/reference/debugprop-info-flags.md)   
 [DBG_ATTRIB_FLAGS](../../../extensibility/debugger/reference/dbg-attrib-flags.md)   
 [IEnumDebugPropertyInfo2](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2.md)