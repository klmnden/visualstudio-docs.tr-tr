---
title: IDebugStackFrame2::GetPhysicalStackRange | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
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
ms.openlocfilehash: 99fc1e635691fa290d0a8e4506ef55d677e9ff78
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62547695"
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
- [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)