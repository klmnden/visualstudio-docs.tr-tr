---
title: IDebugProgram2::EnumCodePaths | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgram2::EnumCodePaths
helpviewer_keywords:
- IDebugProgram2::EnumCodePaths
ms.assetid: fb100c3c-9c29-4d63-bd1f-a3e531cb395f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 09437fddf5cd61aef06341494431c747c4c66c8a
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56681627"
---
# <a name="idebugprogram2enumcodepaths"></a>IDebugProgram2::EnumCodePaths
Kaynak dosyada belirli bir pozisyon için kod yolları bir listesini alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EnumCodePaths( 
   LPCOLESTR            pszHint,
   IDebugCodeContext2*  pStart,
   IDebugStackFrame2*   pFrame,
   BOOL                 fSource,
   IEnumCodePaths2**    ppEnum,
   IDebugCodeContext2** ppSafety
);
```

```csharp
int EnumCodePaths( 
   string                 pszHint,
   IDebugCodeContext2     pStart,
   IDebugStackFrame2      pFrame,
   Int                    fSource,
   out IEnumCodePaths2    ppEnum,
   out IDebugCodeContext2 ppSafety
);
```

#### <a name="parameters"></a>Parametreler
 `pszHint`

 [in] İmleç altındaki **kaynak** veya **ayrıştırılmış kodu** IDE içinde görüntüle.

 `pStart`

 [in] Bir [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) geçerli kod bağlamı temsil eden nesne.

 `pFrame`

 [in] Bir [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md) geçerli kesme noktasıyla ilişkili yığın çerçevesini temsil eden nesne.

 `fSource`

 [in] Sıfır olmayan (`TRUE`) sahipse **kaynak** görünümü veya sıfır (`FALSE`) sahipse **ayrıştırılmış kodu** görünümü.

 `ppEnum`

 [out] Döndürür bir [IEnumCodePaths2](../../../extensibility/debugger/reference/ienumcodepaths2.md) kod yolları bir listesini içeren nesne.

 `ppSafety`

 [out] Döndürür bir [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) atlandı durumda seçilen kod yolu bir kesme noktası ayarlamak için bir ek kod bağlamı temsil eden nesne. Örneğin bu kısa devre yapılma bir Boole ifadesi olması durumunda gerçekleşebilir.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir kod yolu bir yöntem veya programın yürütülmesini geçerli noktayı almak için çağrılan işlev adını açıklar. Çağrı yığınını kod yolları bir listesini gösterir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [IEnumCodePaths2](../../../extensibility/debugger/reference/ienumcodepaths2.md)
- [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)
- [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)