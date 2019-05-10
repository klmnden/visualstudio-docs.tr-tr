---
title: SccUncheckout işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccUncheckout
helpviewer_keywords:
- SccUncheckout function
ms.assetid: 6d498b70-29c7-44b7-ae1c-7e99e488bb09
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6362025f63e4e4f470a7fe107365a59ef99e1e17
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62800299"
---
# <a name="sccuncheckout-function"></a>SccUncheckout İşlevi
Bu işlev, böylece içeriğini seçilen dosyayı veya dosyaları kullanıma alma önce durumu geri önceki bir kullanıma alma işlemi iptal eder. Kullanıma alma beri dosyada yapılan tüm değişiklikler kaybolur.

## <a name="syntax"></a>Sözdizimi

```cpp
SCCRTN SccUncheckout (
   LPVOID    pvContext,
   HWND      hWnd,
   LONG      nFiles,
   LPCSTR*   lpFileNames,
   LONG      fOptions,
   LPCMDOPTS pvOptions
);
```

#### <a name="parameters"></a>Parametreler
 pvContext

[in] Kaynak Denetimi Eklentisi bağlam yapısı.

 hWnd

[in] Kaynak Denetimi Eklentisi sağladığı herhangi bir iletişim kutusu için bir üst öğe olarak kullanabileceğiniz IDE penceresi için bir tanıtıcı.

 nFiles

[in] Belirtilen dosya sayısı `lpFileNames` dizisi.

 lpFileNames

[in] Bir kullanıma almayı geri almak istediğiniz dosyaların tam yerel yol adları dizisi.

 fOptions

[in] Komut bayrakları (kullanılmaz).

 pvOptions

[in] Kaynak denetimi fişi özel seçenekleri.

## <a name="return-value"></a>Dönüş Değeri
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|Kullanıma almayı geri al başarılı oldu.|
|SCC_E_FILENOTCONTROLLED|Seçili dosya kaynak kodu denetimi altında değil.|
|SCC_E_ACCESSFAILURE|Kaynak denetim sistemi, ağ veya çakışma sorunları nedeniyle muhtemelen erişilirken sorun oluştu. Bir yeniden deneme önerilir.|
|SCC_E_NONSPECIFICERROR|Belirli olmayan hata oluştu. Geri alma kullanıma alma başarısız oldu.|
|SCC_E_NOTCHECKEDOUT|Kullanıcının kullanıma alınmış dosyası yok.|
|SCC_E_NOTAUTHORIZED|Kullanıcı bu işlemi gerçekleştirmek için izin verilmiyor.|
|SCC_E_PROJNOTOPEN|Projeyi kaynak denetiminden açılmadı.|
|SCC_I_OPERATIONCANCELED|İşlem tamamlanmadan önce iptal edildi.|

## <a name="remarks"></a>Açıklamalar
 Bu işlem sonrasında `SCC_STATUS_CHECKEDOUT` ve `SCC_STATUS_MODIFIED` bayrakları hem de işaretinin kaldırılması dosyaları kullanıma almayı geri al gerçekleştirildi.

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Denetimi Eklentisi API İşlevleri](../extensibility/source-control-plug-in-api-functions.md)