---
title: IDebugClassField::GetEnclosingClass | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugClassField::GetEnclosingClass
helpviewer_keywords:
- IDebugClassField::GetEnclosingClass method
ms.assetid: a0c12e3c-9ea0-4dfb-9e45-8cea18725022
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 6927a63241e2f2794fb5c70945962e00a1676431
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66329492"
---
# <a name="idebugclassfieldgetenclosingclass"></a>IDebugClassField::GetEnclosingClass
Bu sınıfın kapsayan sınıf alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetEnclosingClass(
    IDebugClassField** ppClassField
);
```

```csharp
int GetEnclosingClass(
    out IDebugClassField ppClassField
);
```

## <a name="parameters"></a>Parametreler
`ppClassField`\
[out] Döndürür bir [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md) sınıfı kapsayan temsil eden nesne. Kapsayan sınıfı yok ise, bir null değer döndürür.

## <a name="return-value"></a>Dönüş Değeri
Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
Bu sınıfın temsil, [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md) nesnedir, iç içe geçmiş bir sınıf sonra `ppClassField` parametresi döndürür bir `IDebugClassField` sınıfı kapsayan temsil eden nesne. Örneğin, bu sınıf tanımını ele alalım:

```
class RootClass {
    class NestedClass { }
};
```

Çağırma `GetEnclosingClass` metodunda `IDebugClassField` nesnesini temsil eden `NestedClass` sınıfı döndürür bir `IDebugClassField` sınıfı temsil eden nesne `RootClass`.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)
