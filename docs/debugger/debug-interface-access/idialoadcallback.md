---
title: Idialoadcallback | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaLoadCallback interface
ms.assetid: 2f18c64c-2cf0-43fc-a447-21e82702ca2a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 353e7dcbe1bcc44b9e8b7e9c7c417913ef07be35
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62828417"
---
# <a name="idialoadcallback"></a>IDiaLoadCallback
Yordamı bulmak, bu nedenle konumu denemesinin ilerleme üzerinde rapor için bir kullanıcı arabirimi etkinleştirme DIA Sembol'nden geri çağırmaları alır.

## <a name="syntax"></a>Sözdizimi

```
IDiaLoadCallback : IUnknown
```

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki yöntemleri bu arabirim tarafından sunulur:

|Yöntem|Açıklama|
|------------|-----------------|
|[IDiaLoadCallback::NotifyDebugDir](../../debugger/debug-interface-access/idialoadcallback-notifydebugdir.md)|Hata ayıklama dizini .exe dosyasında bulundu çağrılır.|
|[IDiaLoadCallback::NotifyOpenDBG](../../debugger/debug-interface-access/idialoadcallback-notifyopendbg.md)|Bir aday .dbg Dosya açıldığında çağrılır.|
|[IDiaLoadCallback::NotifyOpenPDB](../../debugger/debug-interface-access/idialoadcallback-notifyopenpdb.md)|Bir aday .pdb dosyası açıldığında çağrılır.|
|[IDiaLoadCallback::RestrictRegistryAccess](../../debugger/debug-interface-access/idialoadcallback-restrictregistryaccess.md)|Kayıt defteri sorguları sembol arama yollarını bulmak için kullanılabilir olmadığını belirler.|
|[IDiaLoadCallback::RestrictSymbolServerAccess](../../debugger/debug-interface-access/idialoadcallback-restrictsymbolserveraccess.md)|Erişim bir simge sunucusuna simgeleri çözme izin verilip verilmediğini belirler.|

## <a name="remarks"></a>Açıklamalar
 İstemci uygulaması bu arabirimi uygulayan ve çağrısında ona başvuru sağlayan [Idiadatasource::loaddataforexe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md) yöntemi.

 Bir yükleme işlemi uygulanan ek kısıtlamaları için bkz: [Idialoadcallback2](../../debugger/debug-interface-access/idialoadcallback2.md) arabirimi.

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: dia2.h

 Kitaplık: diaguids.lib

 DLL: msdia80.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Arabirimler (Arabirim Erişimi SDK'sında Hata Ayıklama)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)
- [IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)
- [IDiaReadExeAtOffsetCallback](../../debugger/debug-interface-access/idiareadexeatoffsetcallback.md)
- [IDiaReadExeAtRVACallback](../../debugger/debug-interface-access/idiareadexeatrvacallback.md)
- [IDiaLoadCallback2](../../debugger/debug-interface-access/idialoadcallback2.md)