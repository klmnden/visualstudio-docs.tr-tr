---
title: IDebugProgramEngines2::EnumPossibleEngines | Microsoft Docs
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
- IDebugProgramEngines2::EnumPossibleEngines
helpviewer_keywords:
- IDebugProgramEngines2::EnumPossibleEngines
ms.assetid: 993d70a4-f6a5-4e47-a603-0b162b9fde00
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 68e6344e356b085b16311a5d685b019acbd87b70
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49297706"
---
# <a name="idebugprogramengines2enumpossibleengines"></a>IDebugProgramEngines2::EnumPossibleEngines
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu programda hata ayıklamak tüm olası hata ayıklama altyapısı (DE) GUID'lerini döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT EnumPossibleEngines(   
   DWORD  celtBuffer,  
   GUID*  rgguidEngines,  
   DWORD* pceltEngines  
);  
```  
  
```csharp  
int EnumPossibleEngines(   
   uint      celtBuffer,  
   GUID[]    rgguidEngines,  
   ref DWORD pceltEngines  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `celtBuffer`  
 [in] Döndürülecek DE GUID'leri sayısı. Bu ayrıca en büyük boyutunu belirtir `rgguidEngines` dizisi.  
  
 `rgguidEngines`  
 [out içinde] Doldurulacak DE GUID'leri dizisi.  
  
 `pceltEngines`  
 [out] Döndürülen DE GUID'leri gerçek sayısını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür [C++] `HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)` veya [C#] 0x8007007A arabelleğin yeteri kadar büyük değil ise.  
  
## <a name="remarks"></a>Açıklamalar  
 Kaç altyapıları var olduğunu belirlemek için bu yöntemi bir kez çağırın `celtBuffer` parametresi 0 olarak ayarlayın ve `rgguidEngines` parametresi null bir değere ayarlayın. Bu döndürür `HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)` (0x8007007A için C#) ve `pceltEngines` parametresi gerekli arabellek boyutunu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgramEngines2](../../../extensibility/debugger/reference/idebugprogramengines2.md)

