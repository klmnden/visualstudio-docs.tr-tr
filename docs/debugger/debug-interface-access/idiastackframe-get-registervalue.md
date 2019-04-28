---
title: Idiastackframe::get_registervalue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackFrame::get_registerValue method
ms.assetid: cbe3d8ac-319a-40ac-bc3e-4eb81b2d7807
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a819293863b658f6e12609b2c1cd83c37532e02d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62832111"
---
# <a name="idiastackframegetregistervalue"></a>IDiaStackFrame::get_registerValue
Yığın çerçevesi içinde depolanmış olarak belirtilen bir kayıt değeri alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_registerValue(
   ULONG      registerIndex,
   ULONGLONG *pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `registerIndex`

[in] Aşağıdakilerden birini [CV_HREG_e numaralandırması](../../debugger/debug-interface-access/cv-hreg-e.md) sabit listesi değerleri.

 `pRetVal`

[out] Kayıt defterinde depolanan değer.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaStackFrame](../../debugger/debug-interface-access/idiastackframe.md)
- [CV_HREG_e Numaralandırması](../../debugger/debug-interface-access/cv-hreg-e.md)