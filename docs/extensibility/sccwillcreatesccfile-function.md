---
title: SccWillCreateSccFile işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccWillCreateSccFile
helpviewer_keywords:
- SccWillCreateSccFile function
ms.assetid: 0d7542f0-4351-41b3-b24c-960ab99c05a1
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1dc7b9f5b298260b2bcca88c75087059bd8f0065
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66338459"
---
# <a name="sccwillcreatesccfile-function"></a>SccWillCreateSccFile İşlevi
Bu işlev, kaynak denetimi eklentisi MSSCCPRJ oluşturulmasını destekleyip desteklemediğini belirler. SCC dosyası belirli dosyaların her biri için.

## <a name="syntax"></a>Sözdizimi

```cpp
SCCRTN SccWillCreateSccFile(
   LPVOID  pContext,
   LONG    nFiles,
   LPCSTR* lpFileNames,
   LPBOOL  pbSccFiles
);
```

#### <a name="parameters"></a>Parametreler
 pContext

[in] Kaynak Denetimi Eklentisi bağlam işaretçisi.

 nFiles

[in] Dosya adlarını dahil sayısını `lpFileNames` dizi uzunluğu yanı sıra `pbSccFiles` dizisi.

 lpFileNames

[in] Bir dizi kontrol etmek için tam olarak nitelenmiş dosya adını (dizisi gerekir ayrılan çağıran tarafından).

 pbSccFiles

[out içinde] Sonuçları depolanacağı dizisi.

## <a name="return-value"></a>Dönüş Değeri
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|Başarılı.|
|SCC_E_INVALIDFILEPATH|Dizideki yollardan biri geçersiz.|
|SCC_E_NONSPECIFICERROR|Belirli olmayan hata oluştu.|

## <a name="remarks"></a>Açıklamalar
 Bu işlev, kaynak denetimi eklentisi MSSCCPRJ desteği sağlayıp sağlamadığını belirlemek için dosyaların listesiyle birlikte çağrılır. SCC dosya her belirli dosyaları (MSSCCPRJ hakkında daha fazla bilgi. SCC dosya bkz [MSSCCPRJ. SCC dosya](../extensibility/mssccprj-scc-file.md)). Kaynak denetimi eklentileri MSSCCPRJ oluşturma yeteneğine sahip olup olmadığını bildirebilir. SCC dosyaları bildirme `SCC_CAP_SCCFILE` başlatma sırasında. Eklenti döndürür `TRUE` veya `FALSE` dosya başına `pbSccFiles` MSSCCPRJ sahip olduğu belirli dosyaları belirtmek için bir dizi. SCC desteği. Eklenti, işlevden bir başarı kodu döndürürse, dönüş dizideki değerleri dikkate alınır. Hata durumunda, dizi göz ardı edilir.

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Denetimi Eklentisi API İşlevleri](../extensibility/source-control-plug-in-api-functions.md)
- [MSSCCPRJ.SCC Dosyası](../extensibility/mssccprj-scc-file.md)