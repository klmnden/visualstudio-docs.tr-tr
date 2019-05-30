---
title: SccPopulateDirList işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccPopulateDirList
helpviewer_keywords:
- SccPopulateDirList function
ms.assetid: dfff634b-b155-498b-a356-6eb252ac4fad
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9a6508b8cfde2f08eb40201973fec899ee11956b
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66353544"
---
# <a name="sccpopulatedirlist-function"></a>SccPopulateDirList İşlevi
Bu işlev, hangi dizinleri ve (isteğe bağlı olarak) dosyaları incelemek için dizinler listesini verilen kaynak denetiminde depolanmış belirler.

## <a name="syntax"></a>Sözdizimi

```cpp
SCCRTN SccPopulateDirList(
   LPVOID        pContext,
   LONG          nDirs,
   LPCSTR*       lpDirPaths,
   POPDIRLISTFUNCpfnPopulate,
   LPVOID        pvCallerData,
   LONG          fOptions
);
```

#### <a name="parameters"></a>Parametreler
 pContext

[in] Kaynak Denetimi Eklentisi bağlam işaretçisi.

 nDirs

[in] Dizin yolları sayısı `lpDirPaths` dizisi.

 lpDirPaths

[in] İncelemek için dizin yolları dizisi.

 pfnPopulate

[in] Her dizin yolu ve (isteğe bağlı) dosya için çağrılacak bir geri çağırma işlevi `lpDirPaths` (bkz [POPDIRLISTFUNC](../extensibility/popdirlistfunc.md) Ayrıntılar için).

 pvCallerData

[in] Geri çağırma işlevine geçirilecek değer değişmedi.

 fOptions

[in] Dizinleri nasıl işleneceğini denetleyen değerlerinin bir birleşimini ("PopulateDirList bayraklar" bölümüne bakın [kullanılan bit bayrakları tarafından belirli komutları](../extensibility/bitflags-used-by-specific-commands.md) olası değerler için).

## <a name="return-value"></a>Dönüş Değeri
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|İşlem başarıyla tamamlandı.|
|SCC_E_UNKNOWNERROR|Bir hata oluşmuştur.|

## <a name="remarks"></a>Açıklamalar
 Yalnızca bu dizinleri ve (isteğe bağlı olarak) kaynak denetim deposunda olan dosya adlarını geri çağırma işlevine geçirilir.

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Denetimi Eklentisi API İşlevleri](../extensibility/source-control-plug-in-api-functions.md)
- [Özel Komutlar Tarafından Kullanılan Bit Bayrakları](../extensibility/bitflags-used-by-specific-commands.md)
- [POPDIRLISTFUNC](../extensibility/popdirlistfunc.md)
- [Hata Kodları](../extensibility/error-codes.md)