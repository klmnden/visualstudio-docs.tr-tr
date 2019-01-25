---
title: SccEndBatch işlevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- SccEndBatch
helpviewer_keywords:
- SccEndBatch function
ms.assetid: 100e7833-fe0a-45c0-9fca-3e61fd1165b7
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 986056b1f5202c2fb94d27a8792ed3b0fe308944
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54799927"
---
# <a name="sccendbatch-function"></a>SccEndBatch İşlevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu işlev, kaynak denetim işlemlerini toplu burada sona eriyor. Bu toplu bulunmayabilir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
SCCRTN SccEndBatch(void);  
```  
  
#### <a name="parameters"></a>Parametreler  
 Yok.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|SCC_OK|Toplu işlem başarıyla tamamlanmış.|  
|SCC_E_UNKNOWNERROR|Belirli olmayan hata oluştu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Kaynak denetimi toplu birden çok proje veya birden çok bağlamları arasında aynı kaynak denetim işlemlerini yürütmek için kullanılır. Toplu işlemleri, toplu bir işlemi sırasında kullanıcı deneyimini yedekli iletişim kutularından ortadan kaldırmak için kullanılabilir. [SccBeginBatch](../extensibility/sccbeginbatch-function.md) ve `SccEndBatch` işlevi başlangıcını ve bitişini bir işlemin belirtmek için bir çift olarak kullanılır. Bunlar iç içe olamaz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)   
 [SccBeginBatch](../extensibility/sccbeginbatch-function.md)
