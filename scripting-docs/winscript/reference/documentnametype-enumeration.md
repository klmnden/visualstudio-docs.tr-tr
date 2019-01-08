---
title: DOCUMENTNAMETYPE listelemesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- DOCUMENTNAMETYPE
apilocation:
- scrobj.dll
helpviewer_keywords:
- DOCUMENTNAMETYPE enumeration
ms.assetid: d36d550e-efb4-493d-8971-4de267005654
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 31e304cfbb0ed7cd19b832d7ed7c33ccc2c930c3
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54094776"
---
# <a name="documentnametype-enumeration"></a>DOCUMENTNAMETYPE Listelemesi
Bir belge için hangi türün alınacağını açıklar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef enum tagDOCUMENTNAMETYPE {  
   DOCUMENTNAMETYPE_APPNODE,  
   DOCUMENTNAMETYPE_TITLE,  
   DOCUMENTNAMETYPE_FILE_TAIL,  
   DOCUMENTNAMETYPE_URL,  
DOCUMENTNAMETYPE_UNIQUE_TITLE,} DOCUMENTNAMETYPE;  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Açıklama|  
|------------|-----------------|  
|DOCUMENTNAMETYPE_APPNODE|Uygulama ağaçta görünen adını alır.|  
|DOCUMENTNAMETYPE_TITLE|Görüntüleyici başlık çubuğunda görünen adını alır.|  
|DOCUMENTNAMETYPE_FILE_TAIL|Bir yol olmadan dosya adını alır.|  
|DOCUMENTNAMETYPE_URL|Belge URL'sini alır.|  
|DOCUMENTNAMETYPE_UNIQUE_TITLE|Tanımlama için numaralandırma protokolün başlığını alır.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Hata Ayıklayıcı Sabitleri, Sabit Listeleri ve Yapıları](../../winscript/reference/active-script-debugger-constants-enumerations-and-structures.md)