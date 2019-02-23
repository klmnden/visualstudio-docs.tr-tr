---
title: IDebugModOpt | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugModOpt interface
ms.assetid: ebd525e3-d140-4071-9d8c-41871de4125e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c1bbfbc6b6e567e0e56aa369f9c0d1f13a4cbe34
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56690935"
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