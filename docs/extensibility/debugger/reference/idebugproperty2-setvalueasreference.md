---
title: IDebugProperty2::SetValueAsReference | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProperty2::SetValueAsReference
helpviewer_keywords:
- IDebugProperty2::SetValueAsReference method
ms.assetid: 341b1b89-4ab8-4e1c-abe2-fb955df5c6b0
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7b185d284c7b5d5970737fa28aa006c636a6e6f1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54951488"
---
# <a name="idebugproperty2setvalueasreference"></a>IDebugProperty2::SetValueAsReference
Bu özelliğin değeri, belirtilen başvurunun değerini ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT SetValueAsReference(  
   IDebugReference2** rgpArgs,  
   DWORD              dwArgCount,  
   IDebugReference2*  pValue,  
   DWORD              dwTimeout  
);  
```  
  
```csharp  
int SetValueAsReference(  
   IDebugReference2[] rgpArgs,  
   uint               dwArgCount,  
   IDebugReference2   pValue,  
   uint               dwTimeout  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `rgpArgs`  
 [in] Yönetilen kod özellik ayarlayıcı geçirilecek bağımsız değişkenler dizisi. Özellik ayarlayıcısını bağımsız değişken almaz veya bu [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) nesne, böyle bir özellik ayarlayıcı, başvurmuyor `rgpArgs` null bir değer olmalıdır. Bu parametre, genellikle bir null değer olur.  
  
 `dwArgCount`  
 [in] Bağımsız değişken sayısı `rgpArgs` dizisi.  
  
 `pValue`  
 [in] Biçiminde bir başvuru bir [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md) nesnesine bu özelliği ayarlamak için kullanılacak değer.  
  
 `dwTimeout`  
 [in] Değeri, milisaniye cinsinden ayarlamak için yapmanız ne kadar. Tipik bir değer `INFINITE`. Bu, olası tüm değerlendirmesi sürebilir süreyi etkiler.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu, genellikle aşağıdakilerden biri:  
  
|Hata|Açıklama|  
|-----------|-----------------|  
|`E_SETVALUEASREFERENCE_NOTSUPPORTED`|Başvuru değeri ayarı desteklenmiyor.|  
|`E_SETVALUE_VALUE_CANNOT_BE_SET`|Bu özelliği bir yönteme başvuran değeri ayarlanamaz.|  
|`E_SETVALUE_VALUE_IS_READONLY`|Değer salt okunur ve ayarlanamaz.|  
|`E_NOTIMPL`|Yöntem uygulanmadı.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)   
 [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md)