---
title: IDebugEngineProgram2::WatchForThreadStep | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEngineProgram2::WatchForThreadStep
helpviewer_keywords:
- IDebugEngineProgram2::WatchForThreadStep
ms.assetid: b70922a3-1313-409a-b3b7-50c7cd13e394
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 6b3f8db95d6e74a2aa1d146bdd37a66803a8503f
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66345153"
---
# <a name="idebugengineprogram2watchforthreadstep"></a>IDebugEngineProgram2::WatchForThreadStep
Yürütme için izler (veya yürütme için izlemeyi durdurur) belirli bir iş parçacığı üzerinde gerçekleşmesi için.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT WatchForThreadStep( 
   IDebugProgram2* pOriginatingProgram,
   DWORD           dwTid,
   BOOL            fWatch,
   DWORD           dwFrame
);
```

```csharp
int WatchForThreadStep( 
   IDebugProgram2 pOriginatingProgram,
   uint           dwTid,
   int            fWatch,
   uint           dwFrame
);
```

## <a name="parameters"></a>Parametreler
`pOriginatingProgram`\
[in] Bir [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) basamaklı program temsil eden nesne.

`dwTid`\
[in] İzlemek için iş parçacığı tanımlayıcısını belirtir.

`fWatch`\
[in] Sıfır olmayan (`TRUE`) anlamına gelir Başlat tarafından tanımlanan iş parçacığı üzerindeki yürütme için izlemeyi `dwTid`; Aksi takdirde, sıfır (`FALSE`) anlamına gelir, üzerinde yürütme için İzlemeyi Durdur `dwTid`.

`dwFrame`\
[in] Adım türü denetleyen bir çerçeve dizinini belirtir. Bu olduğunda değeri sıfır (0) "adımla" adımı türüdür ve iş parçacığı tarafından tanımlanan her program durması gerektiğini `dwTid` yürütür. Zaman `dwFrame` sıfır olan "Atla" ve yalnızca tarafından iş parçacığı tanıtılan program durması gerektiğini adım türüdür `dwTid` dizini eşit veya daha yığın çerçeve çalışıyor `dwFrame`.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Ne zaman oturum hata ayıklama Yöneticisi (SDM) tarafından tanımlanan, bir program adımları `pOriginatingProgram` parametresi bildirir diğer tüm eklenmiş programlardan bu yöntemi çağırarak.

 Bu yöntem, yalnızca aynı iş parçacığı Adımlama için geçerlidir.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugEngineProgram2](../../../extensibility/debugger/reference/idebugengineprogram2.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)