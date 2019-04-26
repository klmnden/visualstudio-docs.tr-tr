---
title: CV_CFL_LANG | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- CV_CFL_LANG enumeration
ms.assetid: 4e8e0613-ad02-4de9-9f46-e4753c5b0251
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1f02545f1c19b57e46af302fbc0b2abaa7445612
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62555057"
---
# <a name="cvcfllang"></a>CV_CFL_LANG
Bağlantılı modül ve uygulama kaynak kod dilini belirtir.

## <a name="syntax"></a>Sözdizimi

```C++
typedef enum CV_CFL_LANG {
    CV_CFL_C       = 0x00,
    CV_CFL_CXX     = 0x01,
    CV_CFL_FORTRAN = 0x02,
    CV_CFL_MASM    = 0x03,
    CV_CFL_PASCAL  = 0x04,
    CV_CFL_BASIC   = 0x05,
    CV_CFL_COBOL   = 0x06,
    CV_CFL_LINK    = 0x07,
    CV_CFL_CVTRES  = 0x08,
    CV_CFL_CVTPGD  = 0x09,
    CV_CFL_CSHARP  = 0x0A,
    CV_CFL_VB      = 0x0B,
    CV_CFL_ILASM   = 0x0C,
    CV_CFL_JAVA    = 0x0D,
    CV_CFL_JSCRIPT = 0x0E,
    CV_CFL_MSIL    = 0x0F,
    CV_CFL_HLSL    = 0x10
} CV_CFL_LANG;
```

## <a name="elements"></a>Öğeleri
C. CV_CFL_C uygulama dildir

CV_CFL_CXX uygulama dilidir C++.

FORTRAN CV_CFL_FORTRAN uygulama dilidir.

Microsoft Macro Assembler CV_CFL_MASM uygulama dilidir.

Pascal CV_CFL_PASCAL uygulama dilidir.

TEMEL CV_CFL_BASIC uygulama dilidir.

COBOL CV_CFL_COBOL uygulama dilidir.

CV_CFL_LINK uygulama bağlayıcı tarafından oluşturulan bir modüldür.

CVTRES aracıyla dönüştürülen bir kaynak modülü CV_CFL_CVTRES uygulamasıdır.

CV_CFL_CVTPGD uygulama CVTPGD aracıyla oluşturulan POGO en iyi duruma getirilmiş bir modüldür.

CV_CFL_CSHARP uygulama dilidir C#.

Visual Basic CV_CFL_VB uygulama dilidir.

Ara dil derleme (diğer bir deyişle, ortak dil çalışma zamanı (CLR) derleme) CV_CFL_ILASM uygulama dilidir.

Java CV_CFL_JAVA uygulama dilidir.

Jscript CV_CFL_JSCRIPT uygulama dilidir.

CV_CFL_MSIL uygulama dilidir bir bilinmeyen Microsoft Ara dil (MSIL) kullanarak, büyük olasılıkla bir sonuç [/LTCG (bağlama zamanı kodu oluşturma)](/cpp/build/reference/ltcg-link-time-code-generation) geçin.

Yüksek düzey gölgelendirici dili CV_CFL_HLSL uygulama dilidir.

## <a name="remarks"></a>Açıklamalar
Bu numaralandırma değerleri için yapılan bir çağrı tarafından döndürülen [Idiasymbol::get_language](../../debugger/debug-interface-access/idiasymbol-get-language.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: cvconst.h

## <a name="see-also"></a>Ayrıca Bkz.
- [Enumerations and Structures](../../debugger/debug-interface-access/enumerations-and-structures.md)
- [IDiaSymbol::get_language](../../debugger/debug-interface-access/idiasymbol-get-language.md)
