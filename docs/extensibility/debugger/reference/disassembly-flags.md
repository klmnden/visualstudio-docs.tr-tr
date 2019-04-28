---
title: DISASSEMBLY_FLAGS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DISASSEMBLY_FLAGS
helpviewer_keywords:
- DISASSEMBLY_FLAGS enumeration
ms.assetid: c1ec5a4d-5d42-4660-932c-7348550140cb
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0c4602fa1b8d30e9119bb39e925cf7768ae1cbcf
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62924563"
---
# <a name="disassemblyflags"></a>DISASSEMBLY_FLAGS
Ayrıştırılmış kod bayrakları belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_DISASSEMBLY_FLAGS {
    DF_DOCUMENTCHANGE     = 0x00000001,
    DF_DISABLED           = 0x00000002,
    DF_INSTRUCTION_ACTIVE = 0x00000004,
    DF_DATA               = 0x00000008,
    DF_HASSOURCE          = 0x00000010,
    DF_DOCUMENT_CHECKSUM  = 0x00000020
};
typedef DWORD DISASSEMBLY_FLAGS;
```

```csharp
public enum enum_DISASSEMBLY_FLAGS {
    DF_DOCUMENTCHANGE     = 0x00000001,
    DF_DISABLED           = 0x00000002,
    DF_INSTRUCTION_ACTIVE = 0x00000004,
    DF_DATA               = 0x00000008,
    DF_HASSOURCE          = 0x00000010,
    DF_DOCUMENT_CHECKSUM  = 0x00000020
};
```

## <a name="members"></a>Üyeler
DF_DOCUMENTCHANGE, önceki değerinden farklı bir belge bu yönergeyi gösterir.

Bu yönerge yürütülmeyecek DF_DISABLED gösterir.

Bu yönerge, yürütülecek sonraki yönergeleri biridir DF_INSTRUCTION_ACTIVE gösterir (olabilir birden fazla).

DF_DATA, bu yönerge gerçekten veri (kodunda değil) olduğunu gösterir.

Bu yönerge sahip kaynak DF_HASSOURCE gösterir. Profil oluşturma ya da çöp toplama kod gibi bazı yönergeler, karşılık gelen hiçbir kaynak vardır.

DF_DOCUMENT_CHECKSUM gösterir `bstrDocumentUrl` alanı sonra belgesi URL'si sağlama toplamı veri içeriyor. İçin Açıklamalar bölümüne bakın [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md) yapısı için sağlama toplamı veriler nasıl depolanır.

## <a name="remarks"></a>Açıklamalar
Olarak kullanılan `dwFlags` üyesi [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md) yapısı.

Bu bayrak bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md)
