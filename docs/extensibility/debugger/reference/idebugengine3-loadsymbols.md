---
title: IDebugEngine3::LoadSymbols | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEngine3::LoadSymbols
helpviewer_keywords:
- IDebugEngine3::LoadSymbols
ms.assetid: c846a440-1d91-4d48-b8f1-82e902ae152b
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 72c4fce5a7e8dd53093e21db2771d2176462e67c
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66352519"
---
# <a name="idebugengine3loadsymbols"></a>IDebugEngine3::LoadSymbols
Yükleri (gerekirse) Bu hata ayıklama altyapısında hata ayıklaması yapılan tüm modüller için sembolleri.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT LoadSymbols();
```

```csharp
int LoadSymbols();
```

## <a name="parameters"></a>Parametreler
 Yok.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu, bu hata ayıklama altyapısı tarafından başvurulan tüm modüller için hata ayıklama sembolleri yükler. Yalnızca bunlar zaten yüklü olan, semboller yüklenir. Simgeleri bir çağrı tarafından ayarlanmış olduğu yolları üzerinde aranır [SetSymbolPath](../../../extensibility/debugger/reference/idebugengine3-setsymbolpath.md).

## <a name="see-also"></a>Ayrıca bkz.
- [SetSymbolPath](../../../extensibility/debugger/reference/idebugengine3-setsymbolpath.md)
- [IDebugEngine3](../../../extensibility/debugger/reference/idebugengine3.md)