---
title: SccUninitialize işlevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- SccUninitialize
helpviewer_keywords:
- SccUninitialize function
ms.assetid: 17cf5337-d251-4422-bc96-93fe7d48f2ae
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: bcb0b3a6718cc90db6f7176c823ccccbbfc05f9a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54765092"
---
# <a name="sccuninitialize-function"></a>SccUninitialize İşlevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu işlev herhangi bir ayırma veya önceki bir çağrı tarafından oluşturulan açık bağlantıları temizler [Sccınitialize](../extensibility/sccinitialize-function.md) hazırlanırken kaynak denetimi Eklentisi kapatılıyor.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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
 [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)   
 [SccInitialize](../extensibility/sccinitialize-function.md)
