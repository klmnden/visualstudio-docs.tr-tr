---
title: Idialoadcallback::restrictregistryaccess | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- IDiaLoadCallback::RestrictRegistryAccess method
ms.assetid: de4760c3-a746-4bab-8065-1388fed31b67
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fbaa26ab1154b1eea2611a63cf373ea92d095296
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49216251"
---
# <a name="idialoadcallbackrestrictregistryaccess"></a>IDiaLoadCallback::RestrictRegistryAccess
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Kayıt defteri sorguları sembol arama yollarını bulmak için kullanılabilir olmadığını belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT RestrictRegistryAccess();  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Herhangi bir dışındaki kod dönüş `S_OK` simge arama yolu için kayıt defterini sorgulayarak engeller.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaLoadCallback2](../../debugger/debug-interface-access/idialoadcallback2.md)



