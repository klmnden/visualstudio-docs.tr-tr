---
title: IntelliSenseHostFlags | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IntellisenseHostFlags
helpviewer_keywords:
- IntelliSense, IntellisenseHostFlags enumeration
- IntellisenseHostFlags enumeration
ms.assetid: 0930640b-eb84-48ef-a8f7-d4268f55c99c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 882410d68c671a83b13bd14026e5bea4c31cb37e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56683564"
---
# <a name="intellisensehostflags"></a>IntelliSenseHostFlags
IntelliSense konak bayrakları belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum IntellisenseHostFlags
{
    IHF_READONLYCONTEXT      = 0x00000001
    IHF_NOSEPARATESUBJECT    = 0x00000002
    IHF_SINGLELINESUBJECT    = 0x00000004
    IHF_FORCECOMMITTOCONTEXT = 0x00000008
    IHF_OVERTYPE             = 0x00000010
};
```

### <a name="parameters"></a>Parametreler

|Üyeler|Açıklama|
|-------------|-----------------|
|`IHF_READONLYCONTEXT`|Bağlamı arabelleğine salt okunur.|
|`IHF_NOSEPARATESUBJECT`|Konu metin yok. Bağlamı arabelleğine IntelliSense hedef içerir (gelir `!IHF_READONLYCONTEXT`).|
|`IHF_SINGLELINESUBJECT`|Konu metnini çok-satırı özelliğine sahip değil.|
|`IHF_FORCECOMMITTOCONTEXT`|Aynı `CanCommitIntoReadOnlyBuffer`.|
|`IHF_OVERTYPE`|(Konu veya bağlam) düzenleme, üzerine yazma modunda yapılmalıdır.|

## <a name="requirements"></a>Gereksinimler
 SingleFileeditor.idl

## <a name="see-also"></a>Ayrıca bkz.
- <xref:Microsoft.VisualStudio.TextManager.Interop>