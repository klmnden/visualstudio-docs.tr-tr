---
title: IActiveScriptParse32 | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: c39c14aa-beb7-4eca-8b8c-2181da1c2e3e
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
ms.openlocfilehash: 9f44239b4e423588b8455b93b87e4084a9c7d1c4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63009331"
---
# <a name="iactivescriptparse32"></a>IActiveScriptParse32
Windows altyapısı komut dosyasına eklenecek kod kod parçacıklarını ham metni sağlar veya çalışma zamanında değerlendirilecek ifade metin sağlayan komut bunu uygulayan olup `IActiveScriptParse32` arabirimi. VBScript gibi hiçbir bağımsız geliştirme ortamına sahip yorumlanan komut dosyası dilleri için bu alternatif bir mekanizma sağlar (dışında `IPersist*`) komut dosyası altyapısı kod almak ve kod parçacıkları için çeşitli nesne iliştirmek için olaylar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IActiveScriptParse32::AddScriptlet](../../winscript/reference/iactivescriptparse32-addscriptlet.md)|Kod oluşturma yöntemini komut dosyasına ekler.|  
|[IActiveScriptParse32::InitNew](../../winscript/reference/iactivescriptparse32-initnew.md)|Komut dosyası altyapısı başlatır.|  
|[IActiveScriptParse32::ParseScriptText](../../winscript/reference/iactivescriptparse32-parsescripttext.md)|Ad alanına bildirimler ekleyerek ve kodu uygun şekilde değerlendirerek verilen kod oluşturma yöntemini ayrıştırır.|