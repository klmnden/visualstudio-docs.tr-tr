---
title: SccAddFilesFromSCC işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccAddFilesFromSCC
helpviewer_keywords:
- SccAddFilesFromSCC function
ms.assetid: f21a3500-ade8-4dd8-8647-10e2179be9c1
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: cfe58c3eef4b09fccb5cd21b714e5987ae1e08aa
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66333976"
---
# <a name="sccaddfilesfromscc-function"></a>SccAddFilesFromSCC işlevi
Bu işlev, kaynak denetiminden dosyaların listesini açık projeye ekler.

## <a name="syntax"></a>Sözdizimi

```cpp
SCCRTN SccAddFilesFromSCC(
   LPVOID  pContext,
   HWND    hWnd,
   LPSTR   lpUser,
   LPSTR   lpAuxProjPath,
   LONG    cFiles,
   LPCSTR* lpFilePaths,
   LPCSTR  lpDestination,
   LPCSTR  lpComment,
   LPBOOL  pbResults
);
```

### <a name="parameters"></a>Parametreler
 pContext

[in] Kaynak Denetimi Eklentisi bağlam işaretçisi.

 hWnd

[in] Kaynak Denetimi Eklentisi sağladığı herhangi bir iletişim kutusu için bir üst öğe olarak kullanabileceğiniz IDE penceresi için bir tanıtıcı.

 lpUser

[out içinde] Kullanıcı adı (en fazla SCC_USER_SIZE, null sonlandırıcıyı da dahil olmak üzere).

 lpAuxProjPath

[out içinde] Proje tanımlayan yardımcı dize (en fazla `SCC_PRJPATH_`BOYUTU, null sonlandırıcıyı da dahil olmak üzere).

 cFiles

[in] Tarafından verilen dosya sayısı `lpFilePaths`.

 lpFilePaths

[out içinde] Geçerli projeye eklemek için dosya adları dizisi.

 lpDestination

[in] Yazılacak dosyalar nerede hedef yolu.

 lpComment

[in] Eklenmekte olan dosyalar her öğesine uygulanması için açıklama.

 pbResults

[out içinde] Başarılı (sıfır olmayan veya TRUE) olduğunu belirtmek için set ya da hata bayrakları dizisi (sıfır ya da FALSE) her dosya için (dizinin boyutu en az olmalıdır `cFiles` uzun).

## <a name="return-value"></a>Dönüş değeri
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_E_PROJNOTOPEN|Proje açık değil.|
|SCC_E_OPNOTPERFORMED|Bağlantı tarafından belirtildiği gibi aynı projeye değil `lpAuxProjPath.`|
|SCC_E_NOTAUTHORIZED|Veritabanını güncellemek için kullanıcı yetkili değil.|
|SCC_E_NONSPECIFICERROR|Bilinmeyen hata.|
|SCC_I_RELOADFILE|Bir dosya veya projenin yeniden yüklenmesi gerekiyor.|

## <a name="see-also"></a>Ayrıca bkz.
- [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)