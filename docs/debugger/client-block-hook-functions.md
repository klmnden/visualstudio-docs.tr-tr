---
title: İstemci blok kanca işlevleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.hooks
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- client blocks, validating and reporting data
- debugging [C++], hook functions
- _CrtSetDumpClient function
- client blocks, hook functions
- hooks, client block
ms.assetid: f21c197e-565d-4e3f-9b27-4c018c9b87fc
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 900e8db238ee26e0a7015c2acc1741a1917c8cb3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62564079"
---
# <a name="client-block-hook-functions"></a>İstemci Blok Kanca İşlevleri
Doğrulama veya depolanan veriler içeriğini rapor istiyorsanız `_CLIENT_BLOCK` engeller, özellikle bu amaç için bir işlev yazabilirsiniz. Yazdığınız işlevi CRTDBG içinde tanımlanan bir prototip aşağıdakine benzer olması gerekir. Y:

```cpp
void YourClientDump(void *, size_t)
```

 Diğer bir deyişle, kanca işlevini kabul etmelidir bir **void** işaretçi ile birlikte ayırma bloğunun başlangıcına bir **size_t** ayırma boyutunu belirten bir değer yazın ve dönüş`void`. İçeriği size bağlıdır.

 Kanca işlevini kullanarak yükledikten sonra [_CrtSetDumpClient](/cpp/c-runtime-library/reference/crtsetdumpclient), her zaman çağrılacağı bir `_CLIENT_BLOCK` blok yazılan. Ardından [_CrtReportBlockType](/cpp/c-runtime-library/reference/crtreportblocktype) türü veya alt Dökümü alınan bloğu hakkında bilgi edinmek için.

 Geçirdiğiniz, işlev işaretçisi `_CrtSetDumpClient` türünde **_crt_dump_clıent**CRTDBG içinde tanımlanan gibi. Y:

```cpp
typedef void (__cdecl *_CRT_DUMP_CLIENT)
   (void *, size_t);
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Hata Ayıklama Kanca İşlevi Yazma](../debugger/debug-hook-function-writing.md)
- [crt_dbg2 örnek](https://msdn.microsoft.com/library/21e1346a-6a17-4f57-b275-c76813089167)
- [_CrtReportBlockType](/cpp/c-runtime-library/reference/crtreportblocktype)