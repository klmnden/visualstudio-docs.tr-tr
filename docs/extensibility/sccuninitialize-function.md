---
title: SccUninitialize işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccUninitialize
helpviewer_keywords:
- SccUninitialize function
ms.assetid: 17cf5337-d251-4422-bc96-93fe7d48f2ae
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fae6cf7d86d57152446e8acc9e87a0fcbb3d12db
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62433038"
---
# <a name="sccuninitialize-function"></a>SccUninitialize İşlevi
Bu işlev herhangi bir ayırma veya önceki bir çağrı tarafından oluşturulan açık bağlantıları temizler [Sccınitialize](../extensibility/sccinitialize-function.md) hazırlanırken kaynak denetimi Eklentisi kapatılıyor.

## <a name="syntax"></a>Sözdizimi

```cpp
SCCRTN SccUninitialize (
   LPVOID pvContext
);
```

#### <a name="parameters"></a>Parametreler
 pvContext

[in] Kaynak Denetimi Eklentisi bağlam yapısına yönelik oluşturulan [Sccınitialize](../extensibility/sccinitialize-function.md).

## <a name="return-value"></a>Dönüş Değeri
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|Başarıyla tamamlanan temizleme.|

## <a name="remarks"></a>Açıklamalar
 Kaynak Denetimi Eklentisi kapatılması hazırlığı ve bağlam yapısını eklenti ayırdığı bellek boşaltma sorumludur. İşlev, her bir eklentinin belirli örneği için bir kez çağrılır. Bir çağrı [Sccınitialize](../extensibility/sccinitialize-function.md) bu çağrı önce gelir. Proje zaman yapılan çağrının açık olmaya devam edebilir `SccUninitialize`.

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Denetimi Eklentisi API İşlevleri](../extensibility/source-control-plug-in-api-functions.md)
- [SccInitialize](../extensibility/sccinitialize-function.md)