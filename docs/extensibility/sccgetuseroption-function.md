---
title: SccGetUserOption işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccGetUserOption
helpviewer_keywords:
- SccGetUserOption function
ms.assetid: 17863747-1901-4c53-a2b3-ed996085e120
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8b237ded8ac0d22500986a9d390834147f24a2c6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62433194"
---
# <a name="sccgetuseroption-function"></a>SccGetUserOption İşlevi
Bu işlev, çeşitli kullanıcıya özgü seçenekleri alır.

## <a name="syntax"></a>Sözdizimi

```cpp
SCCRTN SccGetUserOption(
   LPVOID pContext,
   LONG nOption,
   LPLONG lpVal
);
```

#### <a name="parameters"></a>Parametreler
 pContext

[in] Kaynak Denetimi Eklentisi bağlam işaretçisi.

 nOption

[in] (Olası seçenekleri için bkz. Notlar) almak için seçenek.

 lpVal

[out] Seçeneği ile ilişkili değer.

## <a name="return-value"></a>Dönüş Değeri
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|Seçenek başarıyla alındı.|
|SCC_E_OPNOTSUPPORTED|seçeneği desteklenmez.|
|SCC_E_NONSPECIFICERROR|Belirtilmeyen bir hata oluştu.|

## <a name="remarks"></a>Açıklamalar
 Aşağıdaki seçenekler, bu komut tarafından desteklenir:

|Kullanıcı seçeneği|Açıklama|
|-----------------|-----------------|
|`SCC_USEROPT_CHECKOUT_LOCALVER`|Kullanıcının dosyaları yerel sürümü kullanıma alma isteyip istemediğini belirler. `lpVal` atanan `SCC_USEROPT_COLV_YES` (kullanıcının istediği yerel dosyaları kullanıma almayı) veya `SCC_USEROPT_COLV_NO`.|

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Denetimi Eklentisi API İşlevleri](../extensibility/source-control-plug-in-api-functions.md)
- [Hata Kodları](../extensibility/error-codes.md)