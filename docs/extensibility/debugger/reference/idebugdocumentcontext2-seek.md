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
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: fbba9b1208ced73c24fbb7050bb4d7e2f8266d52
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66201173"
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

## <a name="parameters"></a>Parametreler
`nCount`\
[in] Deyimleri ya da isterseniz, belge bağlamına bağlı olarak taşımak için satır sayısı.

`ppDocContext`\
[out] Yeni bir [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md) yeni konum nesnesi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)