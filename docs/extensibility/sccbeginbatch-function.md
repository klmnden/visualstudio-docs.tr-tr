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
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: c2e0ae1dd4d01018d9637e5722d8079222afbf3c
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53869132"
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
 [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)   
 [SccEndBatch](../extensibility/sccendbatch-function.md)