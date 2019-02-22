---
title: IDebugDocumentContext2::GetSourceRange | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugDocumentContext2::GetSourceRange
helpviewer_keywords:
- IDebugDocumentContext2::GetSourceRange
ms.assetid: 5903c75e-5390-4d13-9314-1ee276255313
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 206ed65d4374a6dc9ec14d946ae6fabfb0aa3c8c
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56678599"
---
# <a name="idebugdocumentcontext2getsourcerange"></a>IDebugDocumentContext2::GetSourceRange
Bu belge bağlamına kaynak kod aralığını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetSourceRange( 
   TEXT_POSITION* pBegPosition,
   TEXT_POSITION* pEndPosition
);
```

```csharp
int GetSourceRange( 
   TEXT_POSITION[] pBegPosition,
   TEXT_POSITION[] pEndPosition
);
```

#### <a name="parameters"></a>Parametreler
 `pBegPosition`

 [out içinde] A [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md) başlangıç konumu ile doldurulmuş yapısı. Bu bilgiler gerekli değildir, bu bağımsız değişken null bir değere ayarlayın.

 `pEndPosition`

 [out içinde] A [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md) oturum bitiş konumu girilir yapısının. Bu bilgiler gerekli değildir, bu bağımsız değişken null bir değere ayarlayın.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir kaynak aralıktaki tüm kaynak koddan kod katkıda önceki deyiminden sonra yalnızca geçerli deyim arka aralığıdır. Kaynak aralığı genellikle Ayrıştırılmış kod penceresinde kodu, Yorumlar dahil olmak üzere kaynak deyimlerini karıştırmak için kullanılır.

 Yalnızca bu belge bağlamı içinde yer alan kod deyimlerini aralığı almak için arama [GetStatementRange](../../../extensibility/debugger/reference/idebugdocumentcontext2-getstatementrange.md) yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)
- [GetStatementRange](../../../extensibility/debugger/reference/idebugdocumentcontext2-getstatementrange.md)
- [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md)