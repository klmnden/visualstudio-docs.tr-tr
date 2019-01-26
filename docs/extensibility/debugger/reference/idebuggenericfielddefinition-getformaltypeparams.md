---
title: IDebugGenericFieldDefinition::GetFormalTypeParams | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- GetFormalTypeParams
- IDebugGenericFieldDefinition::GetFormalTypeParams
ms.assetid: cadbd6a1-bc7c-4aff-8777-5396b7a23c3e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6490a8ad013907c77d205838db6218a853e717bd
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55029183"
---
# <a name="idebuggenericfielddefinitiongetformaltypeparams"></a>IDebugGenericFieldDefinition::GetFormalTypeParams
Parametre sayısı belirtilen tür parametreleri alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetFormalTypeParams(  
   ULONG32                   cParams,  
   IDebugGenericParamField** ppParams,  
   ULONG32*                  pcParams  
);  
```  
  
```csharp  
int GetFormalTypeParams(  
   uint                          cParams,  
   out IDebugGenericParamField[] ppParams,  
   ref uint                      pcParams  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `cParams`  
 [in] Parametre sayısı.  
  
 `ppParams`  
 [out] Tür parametreleri dizisi.  
  
 `pcParams`  
 [out içinde] Parametre sayısı `ppParams` dizisi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Tür parametreleri sırayla soldan sağa döndür. Örneğin, sözlük\<K, V > IDebugFormalGenericParameters {K, V} döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugGenericFieldDefinition](../../../extensibility/debugger/reference/idebuggenericfielddefinition.md)