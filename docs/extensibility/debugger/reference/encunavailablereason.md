---
title: EncUnavailableReason | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- EncUnavailableReason
helpviewer_keywords:
- EncUnavailableReason enumeration
ms.assetid: c10aa4c0-d7e0-4de1-b8ff-7e050985eb12
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 7db94a181d87791edb242d69b461f90c42a5e080
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66318153"
---
# <a name="encunavailablereason"></a>EncUnavailableReason
`This is for internal use only!` Nedenler temsil eder, **Düzenle ve devam et** kullanılabilir değil.

## <a name="syntax"></a>Sözdizimi

```cpp
enum tagEncUnavailableReason {
    ENCUN_NONE,
    ENCUN_INTEROP,
    ENCUN_SQLCLR,
    ENCUN_MINIDUMP,
    ENCUN_EMBEDDED,
    ENCUN_ATTACH,
    ENCUN_WIN64
};
typedef enum tagEncUnavailableReason EncUnavailableReason;
```

```csharp
public enum EncUnavailableReason {
    ENCUN_NONE,
    ENCUN_INTEROP,
    ENCUN_SQLCLR,
    ENCUN_MINIDUMP,
    ENCUN_EMBEDDED,
    ENCUN_ATTACH,
    ENCUN_WIN64
};
```

## <a name="fields"></a>Alanlar
`ENCUN_NONE`\
Belirli neden neden Düzenle ve devam et kullanılabilir değil.

`ENCUN_INTEROP`\
Düzenle ve devam et kullanılabilir değil bir birlikte çalışabilirlik çağrısı sırasında.

`ENCUN_SQLCLR`\
Düzenle ve devam et kullanılabilir değil, ortak dil çalışma zamanı (CLR) kullanan bir SQL yordam çağrısı sırasında.

`ENCUN_MINIDUMP`\
Düzenle ve devam et kullanılabilir değil bir mini döküm işlenirken.

`ENCUN_EMBEDDED`\
Düzenle ve devam et kullanılamıyor katıştırılmış kod işlerken.

`ENCUN_ATTACH`\
Düzenle ve devam et kullanılamıyor oturum iliştirilmiş olduğundan değil başlatıldığında hata ayıklayıcı tarafından.

`ENCUN_WIN64`\
Düzenle ve devam et kullanılamıyor 64 bit Windows kod işlenirken.

## <a name="remarks"></a>Açıklamalar
Bu iç kullanım için yalnızca göre numaralandırmadır [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)]. [GetENCAvailableState](../../../extensibility/debugger/reference/idebugprocess3-getencavailablestate.md) ve [DisableENC](../../../extensibility/debugger/reference/idebugprocess3-disableenc.md) özel bağlantı noktası sağlayıcısı tarafından uygulanan yöntemleri her zaman döndürmelidir `E_NOTIMPL`.

## <a name="requirements"></a>Gereksinimler
Header: msdbg.idl

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)

- [DisableENC](../../../extensibility/debugger/reference/idebugprocess3-disableenc.md)

- [GetENCAvailableState](../../../extensibility/debugger/reference/idebugprocess3-getencavailablestate.md)
