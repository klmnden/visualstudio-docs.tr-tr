---
title: Idiasession::put_loadaddress | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::put_loadAddress method
ms.assetid: b157b245-1ea0-4b80-8962-d8b278dbc742
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b768b06e0702f7929b402086dcc6e11918f3e683
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56630099"
---
# <a name="idiasessionputloadaddress"></a>IDiaSession::put_loadAddress
Yükleme adresine karşılık gelen yürütülebilir dosyası için sembolleri bu sembol deposu içerisinde ayarlar.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT put_loadAddress ( 
   ULONGLONG NewVal
);
```

#### <a name="parameters"></a>Parametreler
 `NewVal`

[in] Yürütülebilir dosya için adres yükleyin.

## <a name="remarks"></a>Açıklamalar
 Sembol sanal adres (VA) özellikleri, bu yöntem değeri kullanılarak hesaplanır. Bu özellik sıfır olmayan ayarlanmadığı sürece sanal adresleri hesaplanmaz.

> [!NOTE]
>  Aldığınızda, bu yöntemi çağırmanız gerekir [Idiasession](../../debugger/debug-interface-access/idiasession.md) başlamadan önce sanal özellikler üzerinde sembolleri kullanmanız gerekiyorsa nesneyi kullanmayı ve nesne.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSession](../../debugger/debug-interface-access/idiasession.md)