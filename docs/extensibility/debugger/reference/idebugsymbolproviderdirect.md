---
title: IDebugSymbolProviderDirect | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugSymbolProviderDirect interface
ms.assetid: 872b04a8-70de-4ab5-aceb-684c81828545
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1ad8bc95e5fe8fa49088d8c1006bc69243dd4977
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66320369"
---
# <a name="idebugsymbolproviderdirect"></a>IDebugSymbolProviderDirect
Meta verileri ve çekirdek sembol arabirimleri doğrudan erişimi olan bir sembol sağlayıcısını temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugSymbolProviderDirect: IUnknown
```

## <a name="methods"></a>Yöntemler
 Bu arabirim, aşağıdaki yöntemleri uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[GetAppIDFromAddress](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getappidfromaddress.md)|Hata ayıklama adresi verilen uygulama etki alanı tanımlayıcısını alır.|
|[GetCurrentModulesInfo](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getcurrentmodulesinfo.md)|Sembol grubu modülleri hakkında bilgi alır.|
|[GetCurrentModulesState](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getcurrentmodulesstate.md)|Sembol sağlayıcısı üyesi olduğu simgesi grubu hakkındaki bilgileri alır.|
|[GetMetaDataImport](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getmetadataimport.md)|Meta veri alma bilgilerini alır.|
|[GetMethodFromAddress](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getmethodfromaddress.md)|Belirtilen hata ayıklama adresindeki yöntem hakkında bilgi alır.|
|[GetSymUnmanagedReader](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getsymunmanagedreader.md)|Yönetilmeyen kod için simge okuyucu alır.|

## <a name="remarks"></a>Açıklamalar
 Bu arabirim, diğer sembol sağlayıcısı arabirimleri çoğunu yerine kullanılabilir. Meta veriler doğrudan erişim sağlayan ve `CorSym` arabirimleri.

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll