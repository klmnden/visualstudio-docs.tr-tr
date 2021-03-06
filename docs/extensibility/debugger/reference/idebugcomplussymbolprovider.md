---
title: IDebugComPlusSymbolProvider | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugComPlusSymbolProvider interface
ms.assetid: 5b98e908-fd15-49a6-9010-933c9b948085
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4388b3d561420282ade0104443e0db8061ef2ff6
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66352750"
---
# <a name="idebugcomplussymbolprovider"></a>IDebugComPlusSymbolProvider
Yönetilen kod için özel yöntemler ile bir COM + simgesi sağlayıcısını temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugComPlusSymbolProvider : IDebugSymbolProvider
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 İfade değerlendiricisi (EE) için faydalı olan arabirimler ve hata ayıklama altyapısı (DE) tarafından kullanılması amaçlanır o arasında hiçbir ayrım olsa da, aşağıdaki yöntemlerden yalnızca geliştiricileri DE büyük olasılıkla ilginizi çekecek: AreSymbolsLoaded GetAddressesInModuleFromPosition, GetEntryPoint, GetFunctionLineOffset, GetLocalVariableLayout, IsFunctionStale, LoadSymbols, LoadSymbolsFromStream, ReplaceSymbols, UnloadSymbols ve UpdateSymbols.

## <a name="methods"></a>Yöntemler
 Yöntemlere ek olarak [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md) arabirimi bu arabirim, aşağıdaki yöntemleri uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[AreSymbolsLoaded](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-aresymbolsloaded.md)|Uygulama etki alanı tanımlayıcısı verilen Belirtilen modül için hata ayıklama simgeleri yüklü olan belirler.|
|[CreateTypeFromPrimitive](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-createtypefromprimitive.md)|Belirtilen temel türden bir türü oluşturur.|
|[GetAddressesInModuleFromPosition](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-getaddressesinmodulefromposition.md)|Belirtilen modül belge konumda hata ayıklama adresi bir diziye eşler.|
|[GetArrayTypeFromAddress](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-getarraytypefromaddress.md)|Alır, hata ayıklama adresini verilen belirtilen diziye hakkındaki bilgileri yazın.|
|[GetAssemblyName](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-getassemblyname.md)|Modül ve uygulama etki alanı belirtilen derlemenin adını alır.|
|[GetAttributedClassesForLanguage](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-getattributedclassesforlanguage.md)|Belirtilen öznitelik ile belirtilen programlama dilinde uygulanır sınıfları alır.|
|[GetAttributedClassesinModule](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-getattributedclassesinmodule.md)|Belirtilen modüldeki belirtilen özniteliğine sahip sınıf alır.|
|[GetEntryPoint](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-getentrypoint.md)|Uygulama giriş noktasını alır.|
|[GetFunctionLineOffset](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-getfunctionlineoffset.md)|Belirtilen satır sapması temsil eden bir işlev içinde adresi alır.|
|[GetLocalVariablelayout](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-getlocalvariablelayout.md)|Yerel değişkenler için bir dizi yöntem düzenini alır.|
|[GetNameFromToken](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-getnamefromtoken.md)|Belirtilen meta veri nesnesi, verilen belirteçle ilişkili adı döndürür.|
|[GetSymAttribute](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-getsymattribute.md)|Belirtilen modül için belirtilen üst öznitelik ile hata ayıklama sembolleri alır.|
|[GetSymUnmanagedReader](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-getsymunmanagedreader.md)|Yönetilmeyen kod tarafından kullanılacak sembol okuyucu alır.|
|[GetTypeFromAddress](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-gettypefromaddress.md)|Hata ayıklama adresini verilen bir simge türünü alır.|
|[IsFunctionDeleted](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-isfunctiondeleted.md)|Belirtilen hata ayıklama adresten işlevi silinmesi durumunda belirler.|
|[IsFunctionStale](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-isfunctionstale.md)|Belirtilen hata ayıklama adresten işlevi eski olarak kabul edileceğini belirler.|
|[IsHiddenCode](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-ishiddencode.md)|Belirtilen hata ayıklayıcısı adresindeki kod gizli olduğunu belirler.|
|[LoadSymbols](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-loadsymbols.md)|Bellek belirtilen hata ayıklama sembolleri yükler.|
|[LoadSymbolsFromStream](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-loadsymbolsfromstream.md)|Yükleri hata ayıklama simgeleri veri akışını verilir.|
|[ReplaceSymbols](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-replacesymbols.md)|Geçerli hata ayıklama sembolleri, belirtilen veri akışında değerlerle değiştirir.|
|[UnloadSymbols](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-unloadsymbols.md)|Bellek Belirtilen modül için hata ayıklama sembollerini kaldırır.|
|[UpdateSymbols](../../../extensibility/debugger/reference/idebugcomplussymbolprovider-updatesymbols.md)|Hata ayıklama sembolleri bellekte olanlar belirtilen veri akışını güncelleştirir.|

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll