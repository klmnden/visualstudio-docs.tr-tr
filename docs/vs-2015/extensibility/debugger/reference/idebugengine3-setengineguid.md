---
title: IDebugEngine3::SetEngineGuid | Microsoft Docs
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
- IDebugEngine3::SetEngineGuid
helpviewer_keywords:
- IDebugEngine3::SetEngineGuid
ms.assetid: 8bdfa05d-feb7-4d98-abac-77825a04c50f
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 5507cdac8934426aef277c56635e3d378b25e4d9
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49284355"
---
# <a name="idebugengine3setengineguid"></a>IDebugEngine3::SetEngineGuid
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem, hata ayıklama altyapısının (DE) ayarlar `GUID`.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT SetEngineGuid(  
   GUID* guidEngine  
);  
```  
  
```  
[C#]  
int SetEngineGuid(  
   ref Guid guidEngine  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `guidEngine`  
 [in] `GUID` altyapısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugEngine3](../../../extensibility/debugger/reference/idebugengine3.md)

