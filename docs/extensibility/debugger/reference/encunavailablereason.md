---
title: EncUnavailableReason | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- EncUnavailableReason
helpviewer_keywords:
- EncUnavailableReason enumeration
ms.assetid: c10aa4c0-d7e0-4de1-b8ff-7e050985eb12
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7ccc05c58eafe6f8902b3f8ac09b90dc771a3009
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56315696"
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

#### <a name="parameters"></a>Parametreler
ENCUN_NONE  
Belirli neden neden Düzenle ve devam et kullanılabilir değil.

ENCUN_INTEROP  
Düzenle ve devam et kullanılabilir değil bir birlikte çalışabilirlik çağrısı sırasında.

ENCUN_SQLCLR  
Düzenle ve devam et kullanılabilir değil, ortak dil çalışma zamanı (CLR) kullanan bir SQL yordam çağrısı sırasında.

ENCUN_MINIDUMP  
Düzenle ve devam et kullanılabilir değil bir mini döküm işlenirken.

ENCUN_EMBEDDED  
Düzenle ve devam et kullanılamıyor katıştırılmış kod işlerken.

ENCUN_ATTACH  
Düzenle ve devam et kullanılamıyor oturum iliştirilmiş olduğundan değil başlatıldığında hata ayıklayıcı tarafından.

ENCUN_WIN64  
Düzenle ve devam et kullanılamıyor 64 bit Windows kod işlenirken.

## <a name="remarks"></a>Açıklamalar
Bu iç kullanım için yalnızca göre numaralandırmadır [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)]. [GetENCAvailableState](../../../extensibility/debugger/reference/idebugprocess3-getencavailablestate.md) ve [DisableENC](../../../extensibility/debugger/reference/idebugprocess3-disableenc.md) özel bağlantı noktası sağlayıcısı tarafından uygulanan yöntemleri her zaman döndürmelidir `E_NOTIMPL`.

## <a name="requirements"></a>Gereksinimler
Header: msdbg.idl

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)

[DisableENC](../../../extensibility/debugger/reference/idebugprocess3-disableenc.md)

[GetENCAvailableState](../../../extensibility/debugger/reference/idebugprocess3-getencavailablestate.md)

