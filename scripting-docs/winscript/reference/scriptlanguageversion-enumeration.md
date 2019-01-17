---
title: SCRIPTLANGUAGEVERSION sabit listesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 58aa904a-e3ed-41c6-82d6-e91c8279a792
caps.latest.revision: 3
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 374025b7564c058ae89064b6a27384c9075a30f9
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54350108"
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