---
title: Sccqueryınfo işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccQueryInfo
helpviewer_keywords:
- SccQueryInfo function
ms.assetid: 3973d336-a9b7-41a2-a4e6-bb8184a96aaf
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 25a4b9b7d07b74047890c4ba56583cc09a394368
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66353521"
---
# <a name="sccqueryinfo-function"></a>SccQueryInfo İşlevi
Bu işlev, seçili dosyaları kaynak denetimi altında bir dizi için durum bilgilerini alır.

## <a name="syntax"></a>Sözdizimi

```cpp
SCCRTN SccQueryInfo(
   LPVOID  pvContext,
   LONG    nFiles,
   LPCSTR* lpFileNames,
   LPLONG  lpStatus
);
```

#### <a name="parameters"></a>Parametreler
 pvContext

[in] Kaynak Denetimi Eklentisi bağlam yapısı.

 nFiles

[in] Belirtilen dosya sayısı `lpFileNames` dizisi ve uzunluğunu `lpStatus` dizisi.

 lpFileNames

[in] Sorgulanacak dosya adları dizisi.

 lpStatus

[out içinde] Kaynak denetimi eklentisi her dosya için durumu bayrakları döndüren bir dizi. Daha fazla bilgi için [dosya durum kodu](../extensibility/file-status-code-enumerator.md).

## <a name="return-value"></a>Dönüş Değeri
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|Sorgu başarılı oldu.|
|SCC_E_ACCESSFAILURE|Büyük olasılıkla ağ veya çakışma sorunları nedeniyle kaynak denetim sistemine erişen bir sorun oluştu. Bir yeniden deneme önerilir.|
|SCC_E_PROJNOTOPEN|Proje kaynak denetimi altında açık değil.|
|SCC_E_NONSPECIFICERROR|Belirli olmayan hata oluştu.|

## <a name="remarks"></a>Açıklamalar
 Varsa `lpFileName` boş bir dize ise hiçbir durum bilgilerini güncelleştirmek için şu anda yoktur. Aksi halde, tam yolu durum bilgileri değişmiş olabilir dosyasının adıdır.

 Bir bit maskesi, dönüş bir dizi olabilir `SCC_STATUS_xxxx` bitleri. Daha fazla bilgi için [dosya durum kodu](../extensibility/file-status-code-enumerator.md). Bir kaynak denetim sistemi tüm bit türlerini desteklemiyor olabilir. Örneğin, varsa `SCC_STATUS_OUTOFDATE` değil sunulur, bit kümesi değil.

 Bu işlev, dosyaları kullanıma almayı kullanırken aşağıdakileri göz önünde bulundurun `MSSCCI` durumu gereksinimleri:

- `SCC_STATUS_OUTBYUSER` Geçerli kullanıcının dosyayı kullanıma işaretlendiğinde ayarlanır.

- `SCC_STATUS_CHECKEDOUT` sürece ayarlanamaz `SCC_STATUS_OUTBYUSER` ayarlanır.

- `SCC_STATUS_CHECKEDOUT` yalnızca dosya belirlenen çalışma dizinine kullanıma olmadığında ayarlanır.

- Dosya geçerli kullanıcı tarafından çalışma dizini dışındaki bir dizine kullanıma olduysa `SCC_STATUS_OUTBYUSER` ayarlanır ancak `SCC_STATUS_CHECKEDOUT` değil.

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Denetimi Eklentisi API İşlevleri](../extensibility/source-control-plug-in-api-functions.md)
- [Dosya Durumu Kodu](../extensibility/file-status-code-enumerator.md)