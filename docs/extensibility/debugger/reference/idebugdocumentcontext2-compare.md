---
title: IDebugDocumentContext2::Compare | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugDocumentContext2::Compare
helpviewer_keywords:
- IDebugDocumentContext2::Compare
ms.assetid: 2327b1ba-52d0-42fb-a01e-63cb4b332d2f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1416092661ee26bff773ea1a439c241a0f5c5fc6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62921521"
---
# <a name="idebugdocumentcontext2compare"></a>IDebugDocumentContext2::Compare
Bu belge bağlamları belirli bir dizi belge bağlamına karşılaştırır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Compare( 
   DOCCONTEXT_COMPARE       compare,
   IDebugDocumentContext2** rgpDocContextSet,
   DWORD                    dwDocContextSetLen,
   DWORD*                   pdwDocContext
);
```

```csharp
int Compare( 
   enum_ DOCCONTEXT_COMPARE compare,
   IDebugDocumentContext2[] rgpDocContextSet,
   uint                     dwDocContextSetLen,
   out uint                 pdwDocContext
);
```

#### <a name="parameters"></a>Parametreler
 `compare`

 [in] Bir değer [DOCCONTEXT_COMPARE](../../../extensibility/debugger/reference/doccontext-compare.md) karşılaştırma türünü belirten sabit listesi.

 `rgpDocContextSet`

 [in] Bir dizi [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md) karşılaştırılan belge bağlamı temsil eden nesneleri.

 `dwDocContextSetLen`

 [in] Karşılaştırılacak belge bağlamları dizinin uzunluğu.

 `pdwDocContext`

 [out] Dizine döndürür `rgpDocContextSet` karşılaştırmayı ilk belge bağlamı dizisi.

## <a name="return-value"></a>Dönüş Değeri
 Döndürür `S_OK` bir eşleşme bulunmazsa. Döndürür `S_FALSE` eşleşme bulunmazsa. Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md) uygulayan aynı hata ayıklama altyapısı tarafından dizide geçirilen nesneleri uygulanan `IDebugDocumentContext2` üzerinde; Aksi takdirde, çağrılan nesne karşılaştırma geçerli değil.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)
- [DOCCONTEXT_COMPARE](../../../extensibility/debugger/reference/doccontext-compare.md)