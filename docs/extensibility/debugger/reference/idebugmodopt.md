---
title: IDebugModOpt | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugModOpt interface
ms.assetid: ebd525e3-d140-4071-9d8c-41871de4125e
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d9f8fa5e496056eac2a30114f4062f635775350b
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66324037"
---
# <a name="idebugmodopt"></a>IDebugModOpt
Hata ayıklama isteğe bağlı bir değiştirici temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugModOpt : IUnknown
```

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Alınan bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) bir sınıf veya yöntemi temsil eden nesne.

## <a name="methods"></a>Yöntemler
 Bu arabirim, aşağıdaki yöntemi uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[GetModOpts](../../../extensibility/debugger/reference/idebugmodopt-getmodopts.md)|İsteğe bağlı değiştiricilere listesini alır.|

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll