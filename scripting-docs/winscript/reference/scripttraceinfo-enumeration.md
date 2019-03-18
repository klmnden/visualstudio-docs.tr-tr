---
title: SCRIPTTRACEINFO sabit listesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: cb8a4767-8c8e-4fa0-a735-038767a8c500
caps.latest.revision: 3
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2ed2c6566db8209280be7f102a55c7de8cf85c44
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58155816"
---
# <a name="scripttraceinfo-enumeration"></a>SCRIPTTRACEINFO Numaralandırması
İzlenen betik olayı temsil eder. Kullanılan [Iactivescriptsitetraceınfo::sendscripttraceınfo yöntemi](../../winscript/reference/iactivescriptsitetraceinfo-sendscripttraceinfo-method.md).  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef enum tagSCRIPTTRACEINFO {      SCRIPTTRACEINFO_SCRIPTSTART = 0,      SCRIPTTRACEINFO_SCRIPTEND   = 1,      SCRIPTTRACEINFO_COMCALLSTART    = 2,      SCRIPTTRACEINFO_COMCALLEND  = 3,      SCRIPTTRACEINFO_CREATEOBJSTART  = 4,      SCRIPTTRACEINFO_CREATEOBJEND    = 5,      SCRIPTTRACEINFO_GETOBJSTART = 6,      SCRIPTTRACEINFO_GETOBJEND   = 7,  } SCRIPTTRACEINFO ;  
```  
  
## <a name="enumeration-values"></a>Sabit listesi değerleri  
  
|||  
|-|-|  
|SCRIPTTRACEINFO_SCRIPTSTART|Bir komut dosyası başlangıcı.|  
|SCRIPTTRACEINFO_SCRIPTEND|Betiğin sonundaki.|  
|SCRIPTTRACEINFO_COMCALLSTART|Bir COM çağrısı başlangıcı.|  
|SCRIPTTRACEINFO_COMCALLEND|Bir COM çağrısı sonu.|  
|SCRIPTTRACEINFO_CREATEOBJSTART|Nesne oluşturma başlangıcı.|  
|SCRIPTTRACEINFO_CREATEOBJEND|Nesne oluşturma sonu.|  
|SCRIPTTRACEINFO_GETOBJSTART|GetObject çağrı başlangıcı.|  
|SCRIPTTRACEINFO_GETOBJEND|GetObject çağrı sonu.|