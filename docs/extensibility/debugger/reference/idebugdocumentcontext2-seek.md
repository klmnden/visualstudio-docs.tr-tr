---
title: IDebugDocumentContext2::Seek | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugDocumentContext2::Seek
helpviewer_keywords:
- IDebugDocumentContext2::Seek
ms.assetid: 71501356-8a82-4d36-b354-6625bdd2baa0
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: f001eb73e3c24ac1c9f15a4bd2c37c8d2cbe660e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56709531"
---
# <a name="idebugdocumentcontext2seek"></a>IDebugDocumentContext2::Seek
Belge bağlamı belirli sayıda deyimleri veya satırları tarafından taşır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Seek( 
   int                      nCount,
   IDebugDocumentContext2** ppDocContext
);
```

```cpp
int Seek( 
   int                        nCount,
   out IDebugDocumentContext2 ppDocContext
);
```

#### <a name="parameters"></a>Parametreler
 `nCount`

 [in] Deyimleri ya da isterseniz, belge bağlamına bağlı olarak taşımak için satır sayısı.

 `ppDocContext`

 [out] Yeni bir [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md) yeni konum nesnesi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)