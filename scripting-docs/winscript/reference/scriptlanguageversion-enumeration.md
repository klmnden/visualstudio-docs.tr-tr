---
title: SCRIPTLANGUAGEVERSION sabit listesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 58aa904a-e3ed-41c6-82d6-e91c8279a792
caps.latest.revision: 3
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6aab63989d1ae02f7c75fc9c20a14d59e8a05078
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62840219"
---
# <a name="scriptlanguageversion-enumeration"></a>SCRIPTLANGUAGEVERSION Numaralandırması
Sürümleri betik olası belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
typedef enum tagSCRIPTLANGUAGEVERSION{    SCRIPTLANGUAGEVERSION_DEFAULT = 0,    SCRIPTLANGUAGEVERSION_5_7  = 1,    SCRIPTLANGUAGEVERSION_5_8  = 2,    SCRIPTLANGUAGEVERSION_MAX  = 255} SCRIPTLANGUAGEVERSION ;  
```  
  
## <a name="enumeration-values"></a>Sabit listesi değerleri  
  
|||  
|-|-|  
|SCRIPTLANGUAGEVERSION_DEFAULT|Varsayılan sürümü. Tamsayı değeri 0'dır.|  
|SCRIPTLANGUAGEVERSION_5_7|Windows sürümü 5.7 komut dosyası. Tamsayı değeri 1'dir.|  
|SCRIPTLANGUAGEVERSION_5_8|Windows sürüm 5.8 komut dosyası. Tamsayı değeri 2'dir.|  
|SCRIPTLANGUAGEVERSION_MAX|En yüksek sürüm. Tamsayı değeri 255'tir.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Sabitleri, Sabit Listeleri ve Hata Kodları](../../winscript/reference/active-script-constants-enumerations-and-error-codes.md)