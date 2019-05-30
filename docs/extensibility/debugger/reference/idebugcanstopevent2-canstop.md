---
title: IDebugCanStopEvent2::CanStop | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCanStopEvent2::CanStop
helpviewer_keywords:
- IDebugCanStopEvent2::CanStop
ms.assetid: 7d61adbe-6b3d-41f3-86a1-45d9cc01a7f8
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: ab59cf5d077c4e397373c4c86b864ed17749fc19
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66351266"
---
# <a name="idebugcanstopevent2canstop"></a>IDebugCanStopEvent2::CanStop
Hata ayıklama altyapısı (DE) geçerli kod konumda durdurma veya yalnızca yürütme devam gerekip gerekmediğini size bildirir.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT CanStop ( 
   BOOL fCanStop
);
```

```csharp
int CanStop ( 
   int fCanStop
);
```

## <a name="parameters"></a>Parametreler
`fCanStop`\
[in] Sıfır olmayan (`TRUE`) DE geçerli kod konumda; durdurmanız gerekir, aksi takdirde, sıfır (`FALSE`).

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu olay alıcısı genellikle çağrıları [GetReason](../../../extensibility/debugger/reference/idebugcanstopevent2-getreason.md) yöntemi DE istediği durdurmak için nedenini belirlemek için ve çağrıları `IDebugCanStopEvent2::CanStop` uygun yanıtı ile yöntemi.

 DE durursa, durdurma nedenini açıklayan bir olay gönderir. Tarafından temsil edilen bir kullanıcı veya sinyal sonu gönderilir iki olay vardır [IDebugBreakEvent2](../../../extensibility/debugger/reference/idebugbreakevent2.md) arabirimi ve tarafından temsil edilen bir kesme noktası olayının [IDebugBreakpointEvent2](../../../extensibility/debugger/reference/idebugbreakpointevent2.md) arabirimi.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugCanStopEvent2](../../../extensibility/debugger/reference/idebugcanstopevent2.md)
- [IDebugBreakEvent2](../../../extensibility/debugger/reference/idebugbreakevent2.md)
- [IDebugBreakpointEvent2](../../../extensibility/debugger/reference/idebugbreakpointevent2.md)
- [GetReason](../../../extensibility/debugger/reference/idebugcanstopevent2-getreason.md)