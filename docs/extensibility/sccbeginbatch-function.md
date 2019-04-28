---
title: SccBeginBatch işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccBeginBatch
helpviewer_keywords:
- SccBeginBatch function
ms.assetid: 33968183-2e15-4e0d-955b-ca12212d1c25
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 5fd571f967e478b3a03347d6151deb9fc88f62ef
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62433324"
---
# <a name="sccbeginbatch-function"></a>SccBeginBatch işlevi
Bu işlev, kaynak denetim işlemlerini toplu bir dizi başlatır. [SccEndBatch](../extensibility/sccendbatch-function.md) batch sonlandırmak için çağırılır. Bu toplu bulunmayabilir.

## <a name="syntax"></a>Sözdizimi

```cpp
SCCRTN SccBeginBatch(void);
```

### <a name="parameters"></a>Parametreler
 Yok.

## <a name="return-value"></a>Dönüş değeri
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|Toplu işlem başarıyla başladı.|
|SCC_E_UNKNOWNERROR|Belirli olmayan hata oluştu.|

## <a name="remarks"></a>Açıklamalar
 Kaynak denetimi toplu birden çok proje veya birden çok bağlamları arasında aynı işlemleri yürütmek için kullanılır. Toplu işlemleri, toplu bir işlemi sırasında proje başına yedekli iletişim kutularına kullanıcı deneyiminden ortadan kaldırmak için kullanılabilir. `SccBeginBatch` İşlevi ve [SccEndBatch](../extensibility/sccendbatch-function.md) işlevi çift olarak başlangıcını ve bitişini bir işlemin belirtmek için kullanılır. Bunlar iç içe olamaz. `SccBeginBatch` bir toplu işlem sürmekte olduğunu belirten bir bayrak ayarlar.

 Bir toplu işlem etkili olsa da, kaynak denetimi eklentisi en fazla kullanıcı için herhangi bir soru için bir iletişim kutusu sunar ve bu iletişim kutusu yanıtı sonraki tüm işlemleri uygulamak.

## <a name="see-also"></a>Ayrıca bkz.
- [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)
- [SccEndBatch](../extensibility/sccendbatch-function.md)