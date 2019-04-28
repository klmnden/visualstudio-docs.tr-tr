---
title: SccEnumChangedFiles işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccEnumChangedFiles
helpviewer_keywords:
- SccEnumChangedFiles function
ms.assetid: 76cac510-107b-4c1a-ba60-9c39b6db2e71
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: db9bc2738e9a4d7cac0d57b9c613b7070f60baff
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62802911"
---
# <a name="sccenumchangedfiles-function"></a>SccEnumChangedFiles işlevi
Bu işlev yerel dosyaların listesini göz önünde bulundurulduğunda, hangi dosyaların kaynak kod denetimi veritabanında karşılık gelen sürümlerinden farklı olduğunu belirler.

## <a name="syntax"></a>Sözdizimi

```cpp
SCCRTN SccEnumChangedFiles(
   LPVOID  pContext,
   HWND    hWnd,
   LONG    cFiles,
   LPCSTR* lpFileNames,
   LONG*   plIsFileDifferent
);
```

### <a name="parameters"></a>Parametreler
 pContext

[in] Kaynak Denetimi Eklentisi bağlam işaretçisi.

 hWnd

[in] Kaynak Denetimi Eklentisi sağladığı herhangi bir iletişim kutusu için bir üst öğe olarak kullanabileceğiniz IDE penceresi için bir tanıtıcı.

 cFiles

[in] Belirtilen dosya adları sayısını `lpFileNames` dizisi. Ayrıca boyutunu belirtir `plIsFileDifferent` dizisi.

 lpFileNames

[in] Denetlenecek yerel dosya adları dizisi.

 plIsFileDifferent

[out içinde] Her dosya farkı durumunu belirten değerleri dizisi (dizisi en az olmalıdır `cFiles` girişleri). NonZero dosyanın farklı olduğu anlamına gelir.

## <a name="return-value"></a>Dönüş değeri
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|İşlem başarıyla tamamlandı.|
|SCC_UNSPECIFIEDERROR|Genel hata.|

## <a name="see-also"></a>Ayrıca bkz.
- [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)