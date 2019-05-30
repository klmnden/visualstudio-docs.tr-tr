---
title: SccGetUserOption işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccGetUserOption
helpviewer_keywords:
- SccGetUserOption function
ms.assetid: 17863747-1901-4c53-a2b3-ed996085e120
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: eabf9cfc9d878d4d12096c8d264e8ee332031adf
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66353648"
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