---
title: Idiaaddressmap | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaAddressMap interface
ms.assetid: e6467529-508c-4328-85d7-89444ae4d1c1
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 96b24dac472525a711073eccf41355ddb6f10611
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62554241"
---
# <a name="idiaaddressmap"></a>IDiaAddressMap
DIA SDK'sı sanal ve göreli sanal adreslerine hata ayıklama nesneler için nasıl hesaplar üzerinde denetim sağlar.

## <a name="syntax"></a>Sözdizimi

```
IDiaAddressMap : IUnknown
```

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDiaAddressMap`.

|Yöntem|Açıklama|
|------------|-----------------|
|[IDiaAddressMap::get_addressMapEnabled](../../debugger/debug-interface-access/idiaaddressmap-get-addressmapenabled.md)|Belirli bir oturum için bir adres eşlemesi kurulduktan olup olmadığını gösterir.|
|[IDiaAddressMap::put_addressMapEnabled](../../debugger/debug-interface-access/idiaaddressmap-put-addressmapenabled.md)|Adres Haritası sembol adreslerine çevirmek için kullanılıp kullanılmayacağını belirtir.|
|[IDiaAddressMap::get_relativeVirtualAddressEnabled](../../debugger/debug-interface-access/idiaaddressmap-get-relativevirtualaddressenabled.md)|Göreli sanal adreslerine kullanımını ve hesaplama etkin olup olmadığını gösterir.|
|[IDiaAddressMap::put_relativeVirtualAddressEnabled](../../debugger/debug-interface-access/idiaaddressmap-put-relativevirtualaddressenabled.md)|İstemci, etkinleştirme veya devre dışı göreli sanal adreslerine hesaplanması sağlar.|
|[IDiaAddressMap::get_imageAlign](../../debugger/debug-interface-access/idiaaddressmap-get-imagealign.md)|Geçerli resim hizalamasını alır.|
|[IDiaAddressMap::put_imageAlign](../../debugger/debug-interface-access/idiaaddressmap-put-imagealign.md)|Resim hizalamasını ayarlar.|
|[IDiaAddressMap::set_imageHeaders](../../debugger/debug-interface-access/idiaaddressmap-set-imageheaders.md)|Kümeleri göreli sanal adres çevirisi'ni etkinleştirmek için üst görüntü.|
|[IDiaAddressMap::set_addressMap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md)|Görüntü düzen çevirileri desteklemek için bir adres Haritası sağlar.|

## <a name="remarks"></a>Açıklamalar
 Bu arabirim tarafından sağlanan denetimi iki sağladığınız veri kümesi içinde kapsüllenir: görüntü üst bilgileri ve adres eşlemeleri. Çoğu istemciler [Idiadatasource::loaddataforexe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md) yöntemi bir görüntü ve yöntem genellikle tüm verilerin gerekli üst bilgileri ve haritalar kendisini bulabilir uygun hata ayıklama bilgileri bulunamadı. Ancak bazı istemciler, özelleştirilmiş işleme ve verileri için arama uygulayın. Bu gibi istemcilerde yöntemlerini kullanın `IDiaAddressMap` DIA SDK ile arama sonuçları sağlamak için arabirim.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bu arabirim, DIA oturum nesnesinden kullanılabilir. İstemci çağrıları `QueryInterface` arabirimde DIA oturumu nesne, genellikle yöntemi [Idiasession](../../debugger/debug-interface-access/idiasession.md), alınacak `IDiaAddressMap` arabirimi.

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: dia2.h

 Kitaplık: diaguids.lib

 DLL: msdia80.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Arabirimler (Arabirim Erişimi SDK'sında Hata Ayıklama)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)
- [IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)
- [IDiaSession](../../debugger/debug-interface-access/idiasession.md)