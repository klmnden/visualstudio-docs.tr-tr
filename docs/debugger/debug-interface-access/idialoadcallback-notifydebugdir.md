---
title: Idialoadcallback::notifydebugdir | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaLoadCallback::NotifyDebugDir method
ms.assetid: bd04e2f6-0dbf-4742-a556-96f2cd99aa19
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ce251da3c1cb7b1da00971d46cc0801ad24b8985
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62839829"
---
# <a name="idialoadcallbacknotifydebugdir"></a>IDiaLoadCallback::NotifyDebugDir
Hata ayıklama dizini .exe dosyasında bulundu çağrılır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT NotifyDebugDir ( 
   BOOL  fExecutable,
   DWORD cbData,
   BYTE  data[]
);
```

#### <a name="parameters"></a>Parametreler
 `fExecutable`

[in] `TRUE` hata ayıklama dizini, yürütülebilir bir dosya (.dbg Dosya yerine) salt okunur ise.

 `cbData`

[in] Hata ayıklama dizininde bulunan verileri baytlık sayısı.

 `data[]`

[in] Oturum hata ayıklama dizini doldurulmuş bir dizi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Dönüş kodu genellikle göz ardı edilir.

## <a name="remarks"></a>Açıklamalar
 [Idiadatasource::loaddataforexe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md) yürütülebilir dosya işlenirken bir hata ayıklama dizini bulduğunda, bu geri çağırma yöntemini çağırır.

 Bu yöntem, hata ayıklama bilgisi .pdb dosyasında bulunan dışındaki desteklemek için istemcinin ters mühendislik hata ayıklama ve/veya yürütülebilir dosya ihtiyacını ortadan kaldırır. Bu verilerle istemcide kullanılabilir hata ayıklama bilgilerinin türünü ve bu yürütülebilir dosya veya .dbg dosyasında bulunan tanıyabilirsiniz.

 Çoğu istemci çünkü bu geri çağırma gerekmeyeceğinden `IDiaDataSource::loadDataForExe` yöntemi .pdb hem .dbg dosyaları sembolleri sunmak için gerekli olduğunda şeffaf bir şekilde açılır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaLoadCallback2](../../debugger/debug-interface-access/idialoadcallback2.md)
- [IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)