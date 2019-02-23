---
title: IDebugSourceServerModule | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugSourceServerModule interface
ms.assetid: 38213060-451d-46e6-8b4a-efc123e01a2c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c40a2da886b4e999649349d4af306295c87863ff
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56703805"
---
# <a name="idebugsourceservermodule"></a>IDebugSourceServerModule
PDB dosyasında yer alan kaynak sunucu bilgileri temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugSourceServerModule : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Bu arabirim hata ayıklayıcı motoru tarafından uygulanan ve kullanıcı Arabirimi hata ayıklayıcı tarafından tüketilen.

## <a name="methods"></a>Yöntemler
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugSourceServerModule`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetSourceServerData](../../../extensibility/debugger/reference/idebugsourceservermodule-getsourceserverdata.md)|Kaynak sunucu bilgileri alır.|

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll