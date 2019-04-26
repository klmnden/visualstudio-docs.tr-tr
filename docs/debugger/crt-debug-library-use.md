---
title: CRT hata ayıklama kitaplığı kullanımı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- c.debug.runtime
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- /DEBUG linker option [C++]
- crtdbg.h file
- debug library
- MDd compiler option [C++]
- libraries, CRT debug library
- MTd compiler option [C++]
- LDd compiler function [C++]
- /MTd compiler option [C++]
- /MDd compiler option [C++]
- debugging [CRT], CRT debug library
- DEBUG linker option [C++]
- /LDd compiler function [C++]
ms.assetid: 464de16b-4215-4787-9bfa-921aaff9d9f4
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9434be46f357a97ad01f10ceec184ebe6c52eb43
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62565553"
---
# <a name="crt-debug-library-use"></a>CRT Hata Ayıklama Kitaplığı Kullanımı
C çalışma zamanı kitaplığı hata ayıklama kapsamlı destek sağlar. CRT hata ayıklama kitaplıklarını birini kullanmak için ile bağlamalısınız [/DEBUG](/cpp/build/reference/debug-generate-debug-info) ve derleme **/MDd**, **/mtd**, veya **/LDd**.

## <a name="remarks"></a>Açıklamalar
 Ana tanımları ve makroları CRT hata ayıklama için CRTDBG.h üstbilgi dosyasında bulunabilir.

 CRT hata ayıklama kitaplıklarını işlevlerinde hata ayıklama bilgileri ile derlenen ([/z7, / ZD, / zi, /zı (hata ayıklama bilgileri biçimi)](/cpp/build/reference/z7-zi-zi-debug-information-format)) ve en iyi duruma getirme olmadan. Onaylamalar kendisine geçirilen parametreleri doğrulamak için bazı işlevleri içerir ve kaynak kodu sağlanır. Bu kaynak koduyla bekler ve hatalı parametre veya bellek durumları denetlemek gibi işlevleri çalıştığını onaylamak için CRT işlevlerinin geçebilirsiniz. (Bazı CRT teknoloji özel ve kaynak kodu, özel durum işleme, kayan nokta ve diğer birkaç rutinleri için sağlamaz.)

 Visual C++'ı yüklediğinizde, C çalışma zamanı kitaplığı kaynak kodunu sabit diskinize yükleme seçeneğiniz vardır. Kaynak kodu yüklemezseniz, CRT işlevlerinin adımlamak için CD-ROM'dan gerekir.

 Kullanabileceğiniz çeşitli çalışma zamanı kitaplıkları hakkında daha fazla bilgi için bkz. [C çalışma zamanı kitaplıkları](/cpp/c-runtime-library/crt-library-features).

## <a name="see-also"></a>Ayrıca Bkz.

- [CRT Hata Ayıklama Teknikleri](../debugger/crt-debugging-techniques.md)
- [/MD, /MT, /LD (Çalışma Zamanı Kitaplığını Kullan)](/cpp/build/reference/md-mt-ld-use-run-time-library)