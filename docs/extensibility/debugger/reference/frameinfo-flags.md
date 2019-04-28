---
title: FRAMEINFO_FLAGS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- FRAMEINFO_FLAGS
helpviewer_keywords:
- FRAMEINFO_FLAGS enumeration
ms.assetid: 41578062-8455-412a-9d8b-1e1e9dc8d52e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 54bb93fa6f88c02731691728bceacdd4a5fe2036
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62924208"
---
# <a name="frameinfoflags"></a>FRAMEINFO_FLAGS
Bir yığın çerçeve nesnesi hakkında almak için bilgileri belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_FRAMEINFO_FLAGS {
    FIF_FUNCNAME              = 0x00000001,
    FIF_RETURNTYPE            = 0x00000002,
    FIF_ARGS                  = 0x00000004,
    FIF_LANGUAGE              = 0x00000008,
    FIF_MODULE                = 0x00000010,
    FIF_STACKRANGE            = 0x00000020,
    FIF_FRAME                 = 0x00000040,
    FIF_DEBUGINFO             = 0x00000080,
    FIF_STALECODE             = 0x00000100,
    FIF_ANNOTATEDFRAME        = 0x00000200,
    FIF_DEBUG_MODULEP         = 0x00000400,
    FIF_FUNCNAME_FORMAT       = 0x00001000,
    FIF_FUNCNAME_RETURNTYPE   = 0x00002000,
    FIF_FUNCNAME_ARGS         = 0x00004000,
    FIF_FUNCNAME_LANGUAGE     = 0x00008000,
    FIF_FUNCNAME_MODULE       = 0x00010000,
    FIF_FUNCNAME_LINES        = 0x00020000,
    FIF_FUNCNAME_OFFSET       = 0x00040000,
    FIF_FUNCNAME_ARGS_TYPES   = 0x00100000,
    FIF_FUNCNAME_ARGS_NAMES   = 0x00200000,
    FIF_FUNCNAME_ARGS_VALUES  = 0x00400000,
    FIF_FUNCNAME_ARGS_ALL     = 0x00700000,
    FIF_ARGS_TYPES            = 0x01000000,
    FIF_ARGS_NAMES            = 0x02000000,
    FIF_ARGS_VALUES           = 0x04000000,
    FIF_ARGS_ALL              = 0x07000000,
    FIF_ARGS_NOFORMAT         = 0x08000000,
    FIF_ARGS_NO_FUNC_EVAL     = 0x10000000,
    FIF_FILTER_NON_USER_CODE  = 0x20000000,
    FIF_ARGS_NO_TOSTRING      = 0x40000000,
    FIF_DESIGN_TIME_EXPR_EVAL = 0x80000000
};
typedef DWORD FRAMEINFO_FLAGS;
```

```csharp
public enum enum_FRAMEINFO_FLAGS {
    FIF_FUNCNAME              = 0x00000001,
    FIF_RETURNTYPE            = 0x00000002,
    FIF_ARGS                  = 0x00000004,
    FIF_LANGUAGE              = 0x00000008,
    FIF_MODULE                = 0x00000010,
    FIF_STACKRANGE            = 0x00000020,
    FIF_FRAME                 = 0x00000040,
    FIF_DEBUGINFO             = 0x00000080,
    FIF_STALECODE             = 0x00000100,
    FIF_ANNOTATEDFRAME        = 0x00000200,
    FIF_DEBUG_MODULEP         = 0x00000400,
    FIF_FUNCNAME_FORMAT       = 0x00001000,
    FIF_FUNCNAME_RETURNTYPE   = 0x00002000,
    FIF_FUNCNAME_ARGS         = 0x00004000,
    FIF_FUNCNAME_LANGUAGE     = 0x00008000,
    FIF_FUNCNAME_MODULE       = 0x00010000,
    FIF_FUNCNAME_LINES        = 0x00020000,
    FIF_FUNCNAME_OFFSET       = 0x00040000,
    FIF_FUNCNAME_ARGS_TYPES   = 0x00100000,
    FIF_FUNCNAME_ARGS_NAMES   = 0x00200000,
    FIF_FUNCNAME_ARGS_VALUES  = 0x00400000,
    FIF_FUNCNAME_ARGS_ALL     = 0x00700000,
    FIF_ARGS_TYPES            = 0x01000000,
    FIF_ARGS_NAMES            = 0x02000000,
    FIF_ARGS_VALUES           = 0x04000000,
    FIF_ARGS_ALL              = 0x07000000,
    FIF_ARGS_NOFORMAT         = 0x08000000,
    FIF_ARGS_NO_FUNC_EVAL     = 0x10000000,
    FIF_FILTER_NON_USER_CODE  = 0x20000000,
    FIF_ARGS_NO_TOSTRING      = 0x40000000,
    FIF_DESIGN_TIME_EXPR_EVAL = 0x80000000
};
```

## <a name="members"></a>Üyeler
FIF_FUNCNAME başlatma/kullanım `m_bstrFuncName` alan.

FIF_RETURNTYPE başlatma/kullanım `m_bstrReturnType` alan.

FIF_ARGS başlatma/kullanım `m_bstrArgs` alan.

FIF_LANGUAGE başlatma/kullanım `m_bstrLanguage` alan.

FIF_MODULE başlatma/kullanım `m_bstrModule` alan.

FIF_STACKRANGE başlatma/kullanım `m_addrMin` ve `m_addrMax` alanlar (yığın aralığı).

FIF_FRAME başlatma/kullanım `m_pFrame` alan.

FIF_DEBUGINFO başlatma/kullanım `m_fHasDebugInfo` alan.

FIF_STALECODE başlatma/kullanım `m_fStaleCode` alan.

FIF_ANNOTATEDFRAME başlatma/kullanım `m_fAnnotatedFrame` alan.

FIF_DEBUG_MODULEP başlatma/kullanım `m_pModule` alan.

İşlev adı FIF_FUNCNAME_FORMAT biçimlendirir. Sonucun içerisinde geri dönmemiş ise `m_bstrFunName` alan ve başka bir alan doldurulmalıdır.

Ekler için dönüş türü FIF_FUNCNAME_RETURNTYPE `m_bstrFuncName` alan.

FIF_FUNCNAME_ARGS bağımsız değişkenleri ekler `m_bstrFuncName` alan.

FIF_FUNCNAME_LANGUAGE ekler diline `m_bstrFuncName` alan.

Modül adına FIF_FUNCNAME_MODULE ekler `m_bstrFuncName` alan.

FIF_FUNCNAME_LINES ekler için satır sayısı `m_bstrFuncName` alan.

FIF_FUNCNAME_OFFSET ekler `m_bstrFuncName` satırını başından itibaren bayt uzaklığını simgesini `FIF_FUNCNAME_LINES` belirtilir. Varsa `FIF_FUNCNAME_LINES` belirtilmezse veya satır numaralarını kullanılamıyorsa uzaklık bayt cinsinden işlevi başlangıcından ekler.

Ekler için her işlevi bağımsız değişken türünü FIF_FUNCNAME_ARGS_TYPES `m_bstrFuncName` alan.

Her işlev bağımsız değişkeni adını FIF_FUNCNAME_ARGS_NAMES ekler `m_bstrFuncName` alan.

Ekler için her işlevi bağımsız değişkeninin değeri FIF_FUNCNAME_ARGS_VALUES `m_bstrFuncName` alan.

Türü, adı ve tüm bağımsız değişken değeri FIF_FUNCNAME_ARGS_ALL ekler `m_bstrFuncName` alan.

Bağımsız değişken türleri FIF_ARGS_TYPES alınır ve biçimlendirilmiş.

Bağımsız değişken adları FIF_ARGS_NAMES alınır ve biçimlendirilmiş.

Bağımsız değişken değerlerini FIF_ARGS_VALUES alınır ve biçimlendirilmiş.

FIF_ARGS_ALL almak ve biçim türü, adı ve değeri tüm bağımsız değişkenler.

Bağımsız değişkenler FIF_ARGS_NOFORMAT belirtir değil biçimlendirilmiş olmalıdır (örneğin, değil açılış ve kapanış ayraçlarını bağımsız değişken listesi geçici olarak ekleyin ya da bağımsız değişkenler arasındaki ayırıcı ekleyin).

FIF_ARGS_NO_FUNC_EVAL belirten (özellik) değerlendirmesi işlevi bağımsız değişken değerlerini alınırken kullanılmamalıdır.

Hata ayıklama altyapısı FIF_FILTER_NON_USER_CODE dahil edilmez kullanıcı olmayan kod çerçevelerini filtre kullanmaktır.

FIF_ARGS_NO_TOSTRING izin verme `ToString()` İşlev değerlendirmesi veya işlev bağımsız değişkenleri döndürülürken biçimlendirme.

Barındırma işlemi yerine barındırılan uygulama etki FIF_DESIGN_TIME_EXPR_EVAL çerçeve bilgi edinmiş.

## <a name="remarks"></a>Açıklamalar
Bu bayraklar geçirilen [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md) ve [GetInfo](../../../extensibility/debugger/reference/idebugstackframe2-getinfo.md) içinde başlatılacak hangi alanların olduğunu göstermek için yöntemlerini [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) yapıyla veya yapılarla.

Bu bayraklar Ayrıca hangi alanları göstermek için kullanılan [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) yapısı, kullanılan ve geçerli yapısı döndürülür. Bu değerler, bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md)
- [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md)
- [GetInfo](../../../extensibility/debugger/reference/idebugstackframe2-getinfo.md)
