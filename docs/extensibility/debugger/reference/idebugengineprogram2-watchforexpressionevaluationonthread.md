---
title: IDebugEngineProgram2::WatchForExpressionEvaluationOnThread | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEngineProgram2::WatchForExpressionEvaluationOnThread
helpviewer_keywords:
- IDebugEngineProgram2::WatchForExpressionEvaluationOnThread
ms.assetid: 01d05e77-8cac-4d1b-b19f-25756767ed27
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: e72292f403b28c66cddbcee623f27ddfcbe5c3aa
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66345174"
---
# <a name="idebugengineprogram2watchforexpressionevaluationonthread"></a>IDebugEngineProgram2::WatchForExpressionEvaluationOnThread
İfade değerlendirme programı durdurulmuş olsa bile verilen iş parçacığı üzerinde gerçekleşmesi için izin verir (veya izin vermiyor).

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT WatchForExpressionEvaluationOnThread( 
   IDebugProgram2*       pOriginatingProgram,
   DWORD                 dwTid,
   DWORD                 dwEvalFlags,
   IDebugEventCallback2* pExprCallback,
   BOOL                  fWatch
);
```

```csharp
int WatchForExpressionEvaluationOnThread( 
   IDebugProgram2       pOriginatingProgram,
   uint                  dwTid,
   uint                  dwEvalFlags,
   IDebugEventCallback2 pExprCallback,
   int                   fWatch
);
```

## <a name="parameters"></a>Parametreler
`pOriginatingProgram`\
[in] Bir [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) bir ifade değerlendirme programı temsil eden nesne.

`dwTid`\
[in] İş parçacığı tanımlayıcısını belirtir.

`dwEvalFlags`\
[in] Bayraklarının bir birleşimi [EVALFLAGS](../../../extensibility/debugger/reference/evalflags.md) nasıl gerçekleştirilecek bir değerlendirme olduğunu belirten sabit listesi.

`pExprCallback`\
[in] Bir [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) ifadesi değerlendirmesi sırasında oluşan hata ayıklama olayları göndermek için kullanılacak nesne.

`fWatch`\
[in] Sıfır olmayan (`TRUE`), ifade değerlendirmesi tarafından tanımlanan iş parçacığında sağlayan `dwTid`; Aksi takdirde, sıfır (`FALSE`) ifade değerlendirme, iş parçacığı üzerinde izin vermiyor.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Oturum hata ayıklama Yöneticisi (SDM) tarafından tanımlanan, bir program sorduğunda `pOriginatingProgram` parametresi, bir ifadeyi değerlendirmek için bu yöntemi çağırarak diğer tüm eklenmiş programlardan bildirir.

 İfade değerlendirme bir programda başka birinde işlev değerlendirmesi veya tüm değerlendirmesi nedeniyle çalıştırmak için kod neden `IDispatch` özellikleri. Bu nedenle, ifade değerlendirme çalıştırmak ve iş parçacığı bu programa durdurulabilir olsa bile tamamlamak bu yöntem sağlar.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugEngineProgram2](../../../extensibility/debugger/reference/idebugengineprogram2.md)
- [EVALFLAGS](../../../extensibility/debugger/reference/evalflags.md)
- [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)