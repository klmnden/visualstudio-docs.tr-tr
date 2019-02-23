---
title: SccProperties işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccProperties
helpviewer_keywords:
- SccProperties function
ms.assetid: 1bed38c9-73d2-4474-9717-f9dc26a89cbe
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 519a17e7596a9cea479eeb24799724919d49bd45
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56700854"
---
# <a name="sccproperties-function"></a>SccProperties İşlevi
Bu işlev, bir dosya veya proje kaynak denetimi özellikleri görüntüler.

## <a name="syntax"></a>Sözdizimi

```cpp
SCCRTN SccProperties (
   LPVOID pvContext,
   HWND   hWnd,
   LPCSTR lpFileName
);
```

#### <a name="parameters"></a>Parametreler
 pvContext

[in] Kaynak Denetimi Eklentisi bağlam yapısı.

 hWnd

[in] Kaynak Denetimi Eklentisi sağladığı herhangi bir iletişim kutusu için bir üst öğe olarak kullanabileceğiniz IDE penceresi için bir tanıtıcı.

 lpFileName

[in] Dosya ya da proje tam yol adı.

## <a name="return-value"></a>Dönüş Değeri
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|Özellikler başarıyla görüntülendi.|
|SCC_I_RELOADFILE|IDE bu dosyayı yeniden yüklemek için sürüm denetimi sistemi dosya özelliklerini değiştirdi.|
|SCC_E_PROJNOTOPEN|Belirtilen projeyi kaynak denetimine açılmadı.|
|SCC_E_NOTAUTHORIZED|Bu dosya ya da proje özelliklerini görüntülemek için kullanıcı yetkili değil.|
|SCC_E_FILENOTCONTROLLED|Belirtilen dosya veya proje kaynak denetimi altında değil.|
|SCC_E_NONSPECIFICERROR<br /><br /> SCC_E_UNKNOWNERROR|Bilinmeyen veya genel bir hata oluştu.|

## <a name="remarks"></a>Açıklamalar
 Kaynak Denetimi Eklentisi özellikleri kendi iletişim kutusunda görüntülenir.

 Özellikler, kaynak denetimi eklentisi tarafından tanımlanır ve eklentiden eklentiye değişebilir. Eklenti dosyasının kaynak denetimi özelliklerini değiştirmek kullanıcı izin, döndürme zorunluluğu `SCC_I_RELOAD` bu dosya ya da proje yüklenmesi gerekir IDE sinyal.

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Denetimi Eklentisi API İşlevleri](../extensibility/source-control-plug-in-api-functions.md)