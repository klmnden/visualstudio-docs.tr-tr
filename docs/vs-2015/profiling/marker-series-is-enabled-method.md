---
title: marker_series::is_enabled yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- cvmarkersobj/Concurrency::diagnostic::marker_series::is_enabled
helpviewer_keywords:
- Concurrency::diagnostic::marker_series::is_enabled method
ms.assetid: 8ce4dd50-ca29-4c72-98d6-582693f7d501
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 774b1281209787a19cdd83e4ef1019e4bf63591c
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49263802"
---
# <a name="markerseriesisenabled-method"></a>marker_series::is_enabled Yöntemi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Tüm oturum sağlayıcısı etkin olmadığını belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
bool is_enabled();  
bool is_enabled(  
   marker_importance _Importance,  
   int _Category  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `_Importance`  
 Önem düzeyi.  
  
 `_Category`  
 Kategori.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** cvmarkersobj.h  
  
 **Namespace:** Concurrency::diagnostic  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [marker_series Sınıfı](../profiling/marker-series-class.md)



