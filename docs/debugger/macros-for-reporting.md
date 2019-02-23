---
title: Raporlama makroları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.macros
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- macros, CRT reporting macros
- macros, debugging with
- _RPTFn macro
- CRT, reporting macros
- debugging [CRT], reporting macros
- _RPTn macro
ms.assetid: f2085314-a3a8-4caf-a5a4-2af9ad5aad05
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2c92424275a1dff69863b81fbf8567fbc4b84499
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56689297"
---
# <a name="macros-for-reporting"></a>Raporlama Makroları
Kullanabileceğiniz hata ayıklama için **_RPTn** ve **_RPTFn** CRTDBG içinde tanımlı makrolar,. Kullanımını değiştirmek için H `printf` deyimleri. Bunları inclose gerekmez **#ifdef**s, çünkü bunlar otomatik olarak, bu sürümde kaybolur ne zaman yapı **_DEBUG** tanımlanmadı.

|Makrosu|Açıklama|
|-----------|-----------------|
|**_RPT0**, **_RPT1**, **_RPT2**, **_RPT3**, **_RPT4**|Bir ileti dizesi ve sıfır dört bağımsız değişken olarak çıkarır. _RPT1 için **_RPT4**, printf stili bir biçimlendirme dizesi bağımsız değişkenler için ileti dizesi görür.|
|**_RPTF0**, **_RPTF1**, **_RPTF2**, **_RPTF4**|Aynı **_RPTn**, fakat bu makrolar da makro bulunduğu dosyanın adı ve satır numarası çıktı.|

 Aşağıdaki örnek göz önünde bulundurun:

```cpp
#ifdef _DEBUG
    if ( someVar > MAX_SOMEVAR )
        printf( "OVERFLOW! In NameOfThisFunc( ),
               someVar=%d, otherVar=%d.\n",
               someVar, otherVar );
#endif
```

 Bu kodu değerini çıkarır `someVar` ve `otherVar` için **stdout**. Aşağıdaki çağrısını kullanabilirsiniz `_RPTF2` bildirme aynı değerler ve ayrıca, dosya adı ve satır numarası:

```cpp
if (someVar > MAX_SOMEVAR) _RPTF2(_CRT_WARN, "In NameOfThisFunc( ), someVar= %d, otherVar= %d\n", someVar, otherVar );
```

Belirli bir uygulama, C çalışma zamanı kitaplığı ile sağlanan makroları sağlamadığı bildirme hatalarını ayıklama gerektiğini fark edebilirsiniz. Bu durumlarda, özellikle kendi gereksinimlerinizi karşılayacak şekilde tasarlanmış bir makro yazabilirsiniz. Üstbilgi dosyalarınızın her birinde Örneğin, adında bir makro tanımlamak için aşağıdaki gibi kod içerebilir **ALERT_IF2**:

```cpp
#ifndef _DEBUG                  /* For RELEASE builds */
#define  ALERT_IF2(expr, msg, arg1, arg2)  do {} while (0)
#else                           /* For DEBUG builds   */
#define  ALERT_IF2(expr, msg, arg1, arg2) \
    do { \
        if ((expr) && \
            (1 == _CrtDbgReport(_CRT_ERROR, \
                __FILE__, __LINE__, msg, arg1, arg2))) \
            _CrtDbgBreak( ); \
    } while (0)
#endif
```

 Çağrı **ALERT_IF2** tüm işlevleri yapabilirsiniz **printf** kod:

```cpp
ALERT_IF2(someVar > MAX_SOMEVAR, "OVERFLOW! In NameOfThisFunc( ),
someVar=%d, otherVar=%d.\n", someVar, otherVar );
```

 Daha az veya farklı hedeflere rapor için özel bir makro kolaylıkla değiştirebilirsiniz. Hata ayıklama gereksinimleriniz değiştikçe bu yaklaşım özellikle yararlıdır.

## <a name="see-also"></a>Ayrıca Bkz.
- [CRT Hata Ayıklama Teknikleri](../debugger/crt-debugging-techniques.md)
