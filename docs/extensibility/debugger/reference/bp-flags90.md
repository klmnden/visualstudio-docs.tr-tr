---
title: BP_FLAGS90 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- BP_FLAGS90 enumeration
ms.assetid: 3e5a06c5-fb30-4b8a-b2d5-4a0570fc80bd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4d5566de7b54d82da855aa182562f4f6076ec5ae
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56318231"
---
# <a name="bpflags90"></a>BP_FLAGS90
Geçerli değerler için isteğe bağlı bayrakları numaralandırır. İsteğe bağlı bayraklar bir kesme noktası ayarladığınızda ek bilgileri belirtmek için kullanılabilir. Bu numaralandırma genişletir [BP_FLAGS](../../../extensibility/debugger/reference/bp-flags.md) sabit listesi.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_BP_FLAGS90
{
    // VS 8.0 values
    BP90_FLAG_NONE               = 0x0000,
    BP90_FLAG_MAP_DOCPOSITION    = 0x0001,
    BP90_FLAG_DONT_STOP          = 0x0002,

    // Values added in VS 9.0
    BP90_FLAG_TRACEPOINT_CONTINUE = 0x0004,
};
typedef DWORD BP_FLAGS90;
```

```csharp
public enum enum_BP_FLAGS90
{
    // VS 8.0 values
    BP90_FLAG_NONE                = 0x0000,
    BP90_FLAG_MAP_DOCPOSITION     = 0x0001,
    BP90_FLAG_DONT_STOP           = 0x0002,

    // Values added in VS 9.0
    BP90_FLAG_TRACEPOINT_CONTINUE = 0x0004,
};
```

#### <a name="parameters"></a>Parametreler
BP90_FLAG_NONE  
Hiçbir kesme noktası bayrak belirtir.

BP90_FLAG_MAP_DOCPOSITION  
Belge konumu kullanarak hata ayıklama altyapısı (DE) bir kesme noktası eşlemelisiniz belirtir. Bu, yalnızca Active Server Pages (ASP) gibi betik tabanlı kaynak dosyalarında ayarlanan kesme noktaları için geçerlidir.

BP90_FLAG_DONT_STOP  
Kesme noktası hata ayıklama motoru tarafından işlenmesi gerektiğini, ancak hata ayıklama altyapısı sonuçta var. durması gerektiğini değil belirtir. diğer bir deyişle, bir [IDebugBreakpointEvent2](../../../extensibility/debugger/reference/idebugbreakpointevent2.md) olay nesnesi değil gönderilmesi. Bu bayrak öncelikle izleme noktaları ile kullanılmak üzere tasarlanmıştır.

BP90_FLAG_TRACEPOINT_CONTINUE  
Yerel hata ayıklama altyapısı tarafından Adımlama durumu seçili olup olmadığını belirlemek için kullanılır. İzleme noktası makro çalıştırırsa BP90_FLAG_DONT_STOP ayarlanmadığından BP90_FLAG_DONT_STOP farklıdır.

## <a name="requirements"></a>Gereksinimler
Üst bilgi: Msdbg90.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
