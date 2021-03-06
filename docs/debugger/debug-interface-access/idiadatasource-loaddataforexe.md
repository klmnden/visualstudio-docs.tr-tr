---
title: Idiadatasource::loaddataforexe | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaDataSource::loadDataForExe method
ms.assetid: d94a1068-f53f-44b5-b6fb-00dec361a7f2
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4f95e8a9321ff7ae518e72496289f8ad0c7b4682
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62829852"
---
# <a name="idiadatasourceloaddataforexe"></a>IDiaDataSource::loadDataForExe
Açılır ve.exe/.dll dosya ile ilgili hata ayıklama verileri hazırlar.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT loadDataForExe (
   LPCOLESTR executable,
   LPCOLESTR searchPath,
   IUnknown* pCallback
);
```

#### <a name="parameters"></a>Parametreler
yürütülebilir

[in] .Exe veya .dll dosyasının yolu.

searchPath

[in] Hata ayıklama verileri için arama yapmak üzere alternatif yolu.

pCallback

[in] Bir `IUnknown` gibi hata ayıklama geri arama arabirimini destekleyen bir nesne için arabirimi [Idialoadcallback](../../debugger/debug-interface-access/idialoadcallback.md), [Idialoadcallback2](../../debugger/debug-interface-access/idialoadcallback2.md), [Idiareadexeatoffsetcallback](../../debugger/debug-interface-access/idiareadexeatoffsetcallback.md), ve/veya [Idiareadexeatrvacallback](../../debugger/debug-interface-access/idiareadexeatrvacallback.md) arabirimleri.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Aşağıdaki tabloda, bu yöntem için olası hata kodları bazıları gösterilmektedir.

|Değer|Açıklama|
|-----------|-----------------|
|E_PDB_NOT_FOUND|Dosya açılamadı veya dosya geçersiz bir biçime sahip.|
|E_PDB_FORMAT|Bir dosya biçimi geçersiz erişme girişiminde bulunuldu.|
|E_PDB_INVALID_SIG|İmza ile eşleşmiyor.|
|E_PDB_INVALID_AGE|Yaş eşleşmiyor.|
|E_INVALIDARG|Geçersiz parametre.|
|E_UNEXPECTED|Veri kaynağı zaten hazırlandı.|

## <a name="remarks"></a>Açıklamalar
Hata ayıklama.exe/.dll dosya üst ilişkili hata ayıklama veri konumuna adları.

Bu yöntem hata ayıklama üst bilgisini okur ve ardından arar ve hata ayıklama verileri hazırlar. Arama ilerlemesini isteğe bağlı olarak bildirilen ve geri çağırmalar aracılığıyla denetlenir. Örneğin, [Idialoadcallback::notifydebugdir](../../debugger/debug-interface-access/idialoadcallback-notifydebugdir.md) zaman çağrılır `IDiaDataSource::loadDataForExe` yöntemi bulur ve hata ayıklama dizini işler.

[Idiareadexeatoffsetcallback](../../debugger/debug-interface-access/idiareadexeatoffsetcallback.md) ve [Idiareadexeatrvacallback](../../debugger/debug-interface-access/idiareadexeatrvacallback.md) arabirimleri çalıştırılabilir dosyadan veri okumak için alternatif yöntemler sağlamak istemci uygulaması izin dosyası dosyası doğrudan standart dosya g/ç erişilemez.

Doğrulama olmadan bir .pdb dosyası yüklemek için kullanın [Idiadatasource::loaddatafrompdb](../../debugger/debug-interface-access/idiadatasource-loaddatafrompdb.md) yöntemi.

Belirli bir ölçüte göre .pdb dosyasını doğrulamak için kullanın [Idiadatasource::loadandvalidatedatafrompdb](../../debugger/debug-interface-access/idiadatasource-loadandvalidatedatafrompdb.md) yöntemi.

Doğrudan bellekten bir .pdb dosyası yüklemek için kullanın [Idiadatasource::loaddatafromıstream](../../debugger/debug-interface-access/idiadatasource-loaddatafromistream.md) yöntemi.

## <a name="example"></a>Örnek

```C++
class MyCallBack: public IDiaLoadCallback
{
...
};
MyCallBack callback;
...
HRESULT hr = pSource->loadDataForExe( L"myprog.exe", L".\debug", (IUnknown*)&callback);
if (FAILED(hr))
{
    // Report error
}
```

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaDataSource](../../debugger/debug-interface-access/idiadatasource.md)
- [IDiaLoadCallback](../../debugger/debug-interface-access/idialoadcallback.md)
- [IDiaLoadCallback2](../../debugger/debug-interface-access/idialoadcallback2.md)
- [IDiaLoadCallback::NotifyDebugDir](../../debugger/debug-interface-access/idialoadcallback-notifydebugdir.md)
- [IDiaReadExeAtOffsetCallback](../../debugger/debug-interface-access/idiareadexeatoffsetcallback.md)
- [IDiaReadExeAtRVACallback](../../debugger/debug-interface-access/idiareadexeatrvacallback.md)
- [IDiaDataSource::loadDataFromPdb](../../debugger/debug-interface-access/idiadatasource-loaddatafrompdb.md)
- [IDiaDataSource::loadAndValidateDataFromPdb](../../debugger/debug-interface-access/idiadatasource-loadandvalidatedatafrompdb.md)
- [IDiaDataSource::loadDataFromIStream](../../debugger/debug-interface-access/idiadatasource-loaddatafromistream.md)
