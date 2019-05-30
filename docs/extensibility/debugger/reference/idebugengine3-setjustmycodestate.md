---
title: IDebugEngine3::SetJustMyCodeState | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEngine3::SetJustMyCodeState
helpviewer_keywords:
- IDebugEngine3::SetJustMyCodeState
ms.assetid: 8ec17fbf-df93-424a-b2ed-fd1e5ee51256
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: f53b0eb95a2a91f34917b05cadffda2f4aa9a8b1
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66322323"
---
# <a name="idebugengine3setjustmycodestate"></a>IDebugEngine3::SetJustMyCodeState
Bu yöntem, hata ayıklama altyapısı JustMyCode durumu bilgilerini söyler.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT SetJustMyCodeState(
   BOOL           fUpdate,
   DWORD          dwModules,
   JMC_CODE_SPEC* rgJMCSpec
);
```

```csharp
int SetJustMyCodeState(
   int             fUpdate,
   uint            dwModules,
   JMC_CODE_SPEC[] rgJMCSpec
);
```

## <a name="parameters"></a>Parametreler
`fUpdate`\
[in] Sıfır olmayan (`TRUE`) geçerli bilgilerini güncelleştirmek için sıfır (`FALSE`) (önceden ayarlanan yoksayar) tüm bilgileri sıfırlanır.

`dwModules`\
[in] Bilgi yapılarda sayısı `rgJMCSpec.`

`rgJMCSpec`\
[in] Dizi [JMC_CODE_SPEC](../../../extensibility/debugger/reference/jmc-code-spec.md) yapıları kullanılacak.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 JustMyCode olan yalnızca bir kullanıcıya ait kodu hata ayıklama ve sistem kodu gibi tüm ara kod yoksayılıyor kavramı — kaynak kodu, sistem kodunu kullanılabilir olsa bile.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugEngine3](../../../extensibility/debugger/reference/idebugengine3.md)
- [JMC_CODE_SPEC](../../../extensibility/debugger/reference/jmc-code-spec.md)