---
title: SccEndBatch işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccEndBatch
helpviewer_keywords:
- SccEndBatch function
ms.assetid: 100e7833-fe0a-45c0-9fca-3e61fd1165b7
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e0662e4c4d1d71e2c9ae0e8f40ff21868d6b9a5d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62433272"
---
# <a name="sccendbatch-function"></a>SccEndBatch işlevi
Bu işlev, kaynak denetim işlemlerini toplu burada sona eriyor. Bu toplu bulunmayabilir.

## <a name="syntax"></a>Sözdizimi

```cpp
SCCRTN SccEndBatch(void);
```

## <a name="parameters"></a>Parametreler
 Yok.

## <a name="return-value"></a>Dönüş değeri
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|Toplu işlem başarıyla tamamlanmış.|
|SCC_E_UNKNOWNERROR|Belirli olmayan hata oluştu.|

## <a name="remarks"></a>Açıklamalar
 Kaynak denetimi toplu birden çok proje veya birden çok bağlamları arasında aynı kaynak denetim işlemlerini yürütmek için kullanılır. Toplu işlemleri, toplu bir işlemi sırasında kullanıcı deneyimini yedekli iletişim kutularından ortadan kaldırmak için kullanılabilir. [SccBeginBatch](../extensibility/sccbeginbatch-function.md) ve `SccEndBatch` işlevi başlangıcını ve bitişini bir işlemin belirtmek için bir çift olarak kullanılır. Bunlar iç içe olamaz.

## <a name="see-also"></a>Ayrıca bkz.
- [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)
- [SccBeginBatch](../extensibility/sccbeginbatch-function.md)