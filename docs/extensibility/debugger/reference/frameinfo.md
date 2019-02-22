---
title: FRAMEINFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- FRAMEINFO
helpviewer_keywords:
- FRAMEINFO structure
ms.assetid: 95001b89-dddb-45bb-889d-8327994e38a5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 84e7329acb3cdbff5c2f84fbd035867791012b2e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56680509"
---
# <a name="frameinfo"></a>FRAMEINFO
Bir yığın çerçevesini tanımlar.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct tagFRAMEINFO {
    FRAMEINFO_FLAGS    m_dwValidFields;
    BSTR               m_bstrFuncName;
    BSTR               m_bstrReturnType;
    BSTR               m_bstrArgs;
    BSTR               m_bstrLanguage;
    BSTR               m_bstrModule;
    UINT64             m_addrMin;
    UINT64             m_addrMax;
    IDebugStackFrame2* m_pFrame;
    IDebugModule2*     m_pModule;
    BOOL               m_fHasDebugInfo;
    BOOL               m_fStaleCode;
    BOOL               m_fAnnotatedFrame;
} FRAMEINFO;
```

```csharp
public struct FRAMEINFO {
    public uint              m_dwValidFields;
    public string            m_bstrFuncName;
    public string            m_bstrReturnType;
    public string            m_bstrArgs;
    public string            m_bstrLanguage;
    public string            m_bstrModule;
    public ulong             m_addrMin;
    public ulong             m_addrMax;
    public IDebugStackFrame2 m_pFrame;
    public IDebugModule2     m_pModule;
    public int               m_fHasDebugInfo;
    public int               m_fStaleCode;
    public int               m_fAnnotatedFrame;
} FRAMEINFO;
```

## <a name="members"></a>Üyeler
bayrakları birleşimi m_dwValidFields A [FRAMEINFO_FLAGS](../../../extensibility/debugger/reference/frameinfo-flags.md) hangi alanların doldurulur belirten sabit listesi.

m_bstrFuncName işlev adı yığın çerçevesiyle ilgili.

m_bstrReturnType yığın çerçevesiyle ilgili dönüş türü.

m_bstrArgs yığın çerçevesiyle ilgili işlev bağımsız değişkenleri.

Dil m_bstrLanguage içinde hangi işlevi uygulanır.

m_bstrModule modül adı yığın çerçevesiyle ilgili.

en düşük fiziksel yığın adresi m_addrMin.

m_addrMAX fiziksel maksimum yığın adresi.

m_pFrame [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md) Bu yığın çerçevesini temsil eden nesne.

m_pFrame [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md) Bu yığın çerçevesi içeren modül temsil eden nesne.

m_fHasDebugInfo sıfır olmayan (`TRUE`) hata ayıklama bilgileri verilen çerçevede varsa.

m_fHasDebugInfo sıfır olmayan (`TRUE`) yığın çerçevesini artık geçerli değil ve kod ile ilişkili ise.

m_fHasDebugInfo sıfır olmayan (`TRUE`) yığın çerçevesini oturum hata ayıklama Yöneticisi (SDM) tarafından eklenmişse.

## <a name="remarks"></a>Açıklamalar
Bu yapı geçirilir [GetInfo](../../../extensibility/debugger/reference/idebugstackframe2-getinfo.md) doldurulması için yöntemi. Bu yapı ayrıca yer alan bir liste bulunan [IEnumDebugFrameInfo2](../../../extensibility/debugger/reference/ienumdebugframeinfo2.md) hangi sırayla çağrısından döndürülen arabirimi [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [FRAMEINFO_FLAGS](../../../extensibility/debugger/reference/frameinfo-flags.md)
- [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)
- [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md)
- [GetInfo](../../../extensibility/debugger/reference/idebugstackframe2-getinfo.md)
- [IEnumDebugFrameInfo2](../../../extensibility/debugger/reference/ienumdebugframeinfo2.md)
- [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md)
