---
title: SccUninitialize işlevi | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- SccUninitialize
helpviewer_keywords:
- SccUninitialize function
ms.assetid: 17cf5337-d251-4422-bc96-93fe7d48f2ae
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: d3ff6dba6ecbd5b3aeca27222665c1cb1da1ef7b
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49933813"
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

