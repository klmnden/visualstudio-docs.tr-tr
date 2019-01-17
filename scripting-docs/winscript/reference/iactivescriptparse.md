---
title: Iactivescriptparse | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptParse interface
ms.assetid: 8c967d70-f582-4f64-9e79-49f40c4dcb7c
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8325ffcb21f1871ca742611e6587df02ef3b89c8
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54349016"
---
# <a name="iactivescriptparse"></a>IActiveScriptParse
Windows altyapısı komut dosyasına eklenecek kod kod parçacıklarını ham metni sağlar veya çalışma zamanında değerlendirilecek ifade metin sağlayan komut bunu uygulayan olup `IActiveScriptParse` arabirimi. VBScript gibi hiçbir bağımsız geliştirme ortamına sahip yorumlanan komut dosyası dilleri için bu alternatif bir mekanizma sağlar (dışında `IPersist*`) komut dosyası altyapısı kod almak ve kod parçacıkları için çeşitli nesne iliştirmek için olaylar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IActiveScriptParse::InitNew](../../winscript/reference/iactivescriptparse-initnew.md)|Komut dosyası altyapısı başlatır.|  
|[IActiveScriptParse::AddScriptlet](../../winscript/reference/iactivescriptparse-addscriptlet.md)|Kod oluşturma yöntemini komut dosyasına ekler.|  
|[IActiveScriptParse::ParseScriptText](../../winscript/reference/iactivescriptparse-parsescripttext.md)|Ad alanına bildirimler ekleyerek ve kodu uygun şekilde değerlendirerek verilen kod oluşturma yöntemini ayrıştırır.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Arabirimleri](../../winscript/reference/active-script-interfaces.md)