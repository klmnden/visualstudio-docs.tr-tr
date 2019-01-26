---
title: IDebugStackFrame2::GetPhysicalStackRange | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugStackFrame2::GetPhysicalStackRange
helpviewer_keywords:
- IDebugStackFrame2::GetPhysicalStackRange
ms.assetid: 2f6992e2-ac1c-433f-83b7-a7f83a4ce63d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fad5f1936312b91c69377064b17f844ba254f81a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55009732"
---
# <a name="idebugstackframe2getphysicalstackrange"></a>IDebugStackFrame2::GetPhysicalStackRange
Bir yığın çerçevesiyle ilgili olan fiziksel adres aralığını makine bağımlı bir gösterimini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetPhysicalStackRange (   
   UINT64* paddrMin,  
   UINT64* paddrMax  
);  
```  
  
```csharp  
int GetPhysicalStackRange (   
   out ulong paddrMin,  
   out ulong paddrMax  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `paddrMin`  
 [out] Bu yığın çerçevesiyle ilgili en düşük fiziksel adresini döndürür.  
  
 `paddrMax`  
 [out] Bu yığın çerçevesiyle ilgili en yüksek fiziksel adresini döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem tarafından döndürülen bilgileri, yığın çerçevelerini sıralamak için oturum hata ayıklama Yöneticisi (SDM) tarafından kullanılır.  
  
 Bu çağrı yığını, diğer bir deyişle büyüdükçe, yeni yığın çerçevelerini gittikçe daha düşük bellek adreslerinde eklenir varsayılır. Bir çalışma zamanı mimarisi bu varsayımı eşleşen fiziksel yığın aralığı sağlamanız gerekir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)