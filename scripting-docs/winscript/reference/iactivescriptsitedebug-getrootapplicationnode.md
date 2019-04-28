---
title: IActiveScriptSiteDebug::GetRootApplicationNode | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptSiteDebug.GetRootApplicationNode
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptSiteDebug::GetRootApplicationNode
ms.assetid: 2393f566-6b97-47c0-8041-4dd7e3b1d3a3
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 18e603289931115bcaac4d6bb7707b7886f506d4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62992472"
---
# <a name="iactivescriptsitedebuggetrootapplicationnode"></a>IActiveScriptSiteDebug::GetRootApplicationNode
Altında hangi betiği belgelerin eklenmesi gereken uygulama düğümünü alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetRootApplicationNode(  
   IDebugApplicationNode**  ppdanRoot  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppdanRoot`  
 [out] Betik belgelerini tutan hata ayıklama uygulama düğümü. Olabilir `NULL`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, betik belgelerini altında eklenmesi gereken uygulama düğümü döndürür. Yöntem döndürebilir `NULL` için `ppdanRoot` betik belgelerini en üst düzey gerekiyorsa.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptSiteDebug Arabirimi](../../winscript/reference/iactivescriptsitedebug-interface.md)