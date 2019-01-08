---
title: Ijsdebugframe arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 5af46b18-9d25-4a23-b8d1-fa23bea3efcf
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2fa491a02d289a0a92a70348ec5ef483dd8f8467
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54093309"
---
# <a name="ijsdebugframe-interface"></a>IJsDebugFrame Arabirimi
Bir yığın çerçevesini temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
IJsDebugFrame : public IUnknown;  
```  
  
## <a name="members"></a>Üyeler  
  
### <a name="public-methods"></a>Ortak Yöntemler  
  
|Ad|Açıklama|  
|----------|-----------------|  
|[IJsDebugFrame::Evaluate Metodu](../../winscript/reference/ijsdebugframe-evaluate-method.md)|Bu yığın çerçevesi bağlamında bir ifade değerlendirin.|  
|[IJsDebugFrame::GetDebugProperty Metodu](../../winscript/reference/ijsdebugframe-getdebugproperty-method.md)|Bu yığın çerçevesi için bir özellik tarayıcısı döndürür.|  
|[IJsDebugFrame::GetDocumentPositionWithId Metodu](../../winscript/reference/ijsdebugframe-getdocumentpositionwithid-method.md)|Bu yığın çerçevesinin kullanıcı düzeyi belge içindeki konumunu döndürür.|  
|[IJsDebugFrame::GetDocumentPositionWithName Metodu](../../winscript/reference/ijsdebugframe-getdocumentpositionwithname-method.md)|Bu yığın çerçevesinin kullanıcı düzeyi belge içindeki konumunu döndürür.|  
|[IJsDebugFrame::GetName Metodu](../../winscript/reference/ijsdebugframe-getname-method.md)|Yığın çerçevesinin kullanıcı dostu adını alır.|  
|[IJsDebugFrame::GetReturnAddress Metodu](../../winscript/reference/ijsdebugframe-getreturnaddress-method.md)|'Başında' itilmiş dönüş adresi alır (bkz: GetStackRange) çerçevesi.|  
|[IJsDebugFrame::GetStackRange Metodu](../../winscript/reference/ijsdebugframe-getstackrange-method.md)|Mantıksal JavaScript yığın çerçevesinin mutlak adres aralığını döndürür.|  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Windows Betik Arabirimleri Başvurusu](../../winscript/reference/windows-script-interfaces-reference.md)