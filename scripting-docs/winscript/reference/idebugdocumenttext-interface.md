---
title: Idebugdocumenttext arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugDocumentText interface
ms.assetid: 242bad79-9c0a-4a30-879a-9f43db4e022b
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8878e1ce6e9ad05fc94b134a2e71847b67d578d2
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63008621"
---
# <a name="idebugdocumenttext-interface"></a>IDebugDocumentText Arabirimi
Hata ayıklama belge salt metin sürümüne erişim sağlar. Bu arabirim, aşağıdaki kuralları kullanır:  
  
- Sıfır tabanlı karakter konumlarının hem satır numaraları olan.  
  
- Karakter konumlarının karakter ofsetleri temsil eder; Bunlar değil baytını temsil eden veya uzaklıkları word. Win32 için bir karakter konumunu bir Unicode uzaklık dayalıdır.  
  
  Devralınan yöntemleri yanı sıra `IDebugDocument`, `IDebugDocumentText` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugDocumentText::GetDocumentAttributes](../../winscript/reference/idebugdocumenttext-getdocumentattributes.md)|Belgenin özniteliklerini döndürür.|  
|[IDebugDocumentText::GetSize](../../winscript/reference/idebugdocumenttext-getsize.md)|Belgede, satır sayısı ve karakter sayısını döndürür.|  
|[IDebugDocumentText::GetPositionOfLine](../../winscript/reference/idebugdocumenttext-getpositionofline.md)|Karakter konumunu bir satırın ilk karaktere karşılık gelen döndürür.|  
|[IDebugDocumentText::GetLineOfPosition](../../winscript/reference/idebugdocumenttext-getlineofposition.md)|Satır numarası ve isteğe bağlı olarak, karşılık gelen satır karakter kaydırma için belirli karakter konumunu döndürür.|  
|[IDebugDocumentText::GetText](../../winscript/reference/idebugdocumenttext-gettext.md)|Karakterler ve/veya bir karakter konumu aralıkla ilişkili karakter özniteliklerini alır.|  
|[IDebugDocumentText::GetPositionOfContext](../../winscript/reference/idebugdocumenttext-getpositionofcontext.md)|Karşılık gelen bir belge bağlamına aralığın karakter konumunu döndürür.|  
|[IDebugDocumentText::GetContextOfPosition](../../winscript/reference/idebugdocumenttext-getcontextofposition.md)|Belirtilen karakter konumu aralığına karşılık gelen bir belge bağlam nesnesi oluşturur.|