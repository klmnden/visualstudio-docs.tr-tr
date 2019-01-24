---
title: SccGetVersion işlevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- SccGetVersion
helpviewer_keywords:
- SccGetVersion function
ms.assetid: a6e786bf-744e-4272-9e21-0be44d23b1a1
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: a4e548f1f2b82a97206cdf41174a8c1c7d61e885
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54763788"
---
# <a name="sccgetversion-function"></a>SccGetVersion İşlevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu işlev, kaynak denetimi eklentisi tarafından desteklenen kaynak denetimi eklentisi API sürüm numarasını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
LONG SccGetVersion(void);  
```  
  
#### <a name="parameters"></a>Parametreler  
 Yok.  
  
## <a name="return-value"></a>Dönüş Değeri  
 A `LONG` desteklenen kaynak denetimi eklentisi API sürüm numarasını içeren veri türü:  
  
|WORD|Açıklama|  
|----------|-----------------|  
|GET_Y_LPARAM KULLANIN|Ana sürüm|  
|GET_X_LPARAM|Alt sürüm|  
  
## <a name="remarks"></a>Açıklamalar  
 Örneğin, bir kaynak denetimi Eklentisi Kaynak Denetimi Eklentisi API sürümü 1.3 destekliyorsa, bu işlev 0x0103 döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentisi API İşlevleri](../extensibility/source-control-plug-in-api-functions.md)
