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
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 341a4d2da740d2907172fb7761dc0c18d13d1456
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65457275"
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

## <a name="parameters"></a>Parametreler
 `paddrMin`\

 [out] Bu yığın çerçevesiyle ilgili en düşük fiziksel adresini döndürür.

 `paddrMax`\

 [out] Bu yığın çerçevesiyle ilgili en yüksek fiziksel adresini döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem tarafından döndürülen bilgileri, yığın çerçevelerini sıralamak için oturum hata ayıklama Yöneticisi (SDM) tarafından kullanılır.

 Bu çağrı yığını, diğer bir deyişle büyüdükçe, yeni yığın çerçevelerini gittikçe daha düşük bellek adreslerinde eklenir varsayılır. Bir çalışma zamanı mimarisi bu varsayımı eşleşen fiziksel yığın aralığı sağlamanız gerekir.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)