---
title: IDebugGenericFieldDefinition::ConstructInstantiation | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- ConstructInstantiation
- IDebugGenericFieldDefinition::ConstructInstantiation
ms.assetid: ef8ae261-a98b-4dc2-93b3-7c5191818ba2
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 83284124f4cdf2fce49812998b6444fa43dc958e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54954949"
---
# <a name="idebuggenericfielddefinitionconstructinstantiation"></a>IDebugGenericFieldDefinition::ConstructInstantiation
Tür bağımsız değişkenleri dizisini verilen bir alanda örneği oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT ConstructInstantiation(  
   ULONG32       cArgs,  
   IDebugField** ppArgs,  
   IDebugField** ppConstructedField  
);  
```  
  
```csharp  
int ConstructInstantiation(  
   uint            cArgs,  
   IDebugField[]   ppArgs,  
   out IDebugField ppConstructedField  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `cArgs`  
 [in] Bağımsız değişken sayısı `ppArgs` dizisi.  
  
 `ppArgs`  
 [in] Tür bağımsız değişkenleri içeren bir dizi. Tür bağımsız değişkenlerini kapalı türler (genel olmayan veya tümüyle izlenen genel türler) olmalıdır.  
  
 `ppConstructedField`  
 [out] Döndürür [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) yeni alanını temsil eden arabirim.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Kısıtlamaları denetlenmez.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugGenericFieldDefinition](../../../extensibility/debugger/reference/idebuggenericfielddefinition.md)