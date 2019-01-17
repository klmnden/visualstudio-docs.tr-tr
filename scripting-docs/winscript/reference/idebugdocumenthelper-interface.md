---
title: Idebugdocumenthelper arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugDocumentHelper interface
ms.assetid: b652a31e-b87b-45f1-b586-94f2b6e822db
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8fdb153a81d63a7a6cffd0b42001405ecfb87596
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54346988"
---
# <a name="idebugdocumenthelper-interface"></a>IDebugDocumentHelper Arabirimi
Akıllı barındırmak için gereken birçok arabirimler için uygulamaları sağlayın `IDebugDocument`, `IDebugDocumentContext`, `IDebugDocumentProvider`, `IDebugDocumentText`, ve `IDebugDocumentTextEvents` arabirimleri.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IDebugDocumentHelper` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugDocumentHelper::Init](../../winscript/reference/idebugdocumenthelper-init.md)|Hata ayıklama belge yardımcı bir ad ve ilk öznitelikleri ile başlatır.|  
|[IDebugDocumentHelper::Attach](../../winscript/reference/idebugdocumenthelper-attach.md)|Bu belge için belge ağacı ekler.|  
|[IDebugDocumentHelper::Detach](../../winscript/reference/idebugdocumenthelper-detach.md)|Bu belge, belge ağacından kaldırır.|  
|[IDebugDocumentHelper::AddUnicodeText](../../winscript/reference/idebugdocumenthelper-addunicodetext.md)|Bir Unicode dize sonuna ekler, bu belgenin.|  
|[IDebugDocumentHelper::AddDBCSText](../../winscript/reference/idebugdocumenthelper-adddbcstext.md)|Bir DBCS dize sonuna ekler, bu belgenin.|  
|[IDebugDocumentHelper::SetDebugDocumentHost](../../winscript/reference/idebugdocumenthelper-setdebugdocumenthost.md)|Kümeleri `IDebugDocumentHost` bu belge için.|  
|[IDebugDocumentHelper::AddDeferredText](../../winscript/reference/idebugdocumenthelper-adddeferredtext.md)|Verilen metni kullanılabilir, ancak karakterleri sağlamaz yardımcı bildirir.|  
|[IDebugDocumentHelper::DefineScriptBlock](../../winscript/reference/idebugdocumenthelper-definescriptblock.md)|Belirtilen betik altyapısı tarafından işlenen bir betik bloğu, belirli bir karakter aralığı Yardımcısı için belirtir.|  
|[IDebugDocumentHelper::SetDefaultTextAttr](../../winscript/reference/idebugdocumenthelper-setdefaulttextattr.md)|Bir betik bloğu içinde olmayan metin için kullanılacak varsayılan öznitelikleri ayarlar.|  
|[IDebugDocumentHelper::SetTextAttributes](../../winscript/reference/idebugdocumenthelper-settextattributes.md)|Öznitelikler, bir metin aralığı ayarlar.|  
|[IDebugDocumentHelper::SetLongName](../../winscript/reference/idebugdocumenthelper-setlongname.md)|Belge için uzun adını ayarlar.|  
|[IDebugDocumentHelper::SetShortName](../../winscript/reference/idebugdocumenthelper-setshortname.md)|Kısa ad belge için ayarlar.|  
|[IDebugDocumentHelper::SetDocumentAttr](../../winscript/reference/idebugdocumenthelper-setdocumentattr.md)|Bu belge için öznitelikleri ayarlar.|  
|[IDebugDocumentHelper::GetDebugApplicationNode](../../winscript/reference/idebugdocumenthelper-getdebugapplicationnode.md)|Bu belgeye karşılık gelen hata ayıklama uygulama düğümü döndürür.|  
|[IDebugDocumentHelper::GetScriptBlockInfo](../../winscript/reference/idebugdocumenthelper-getscriptblockinfo.md)|Bir dizi karakter ve karşılık gelen bir betik bloğu için komut dosyası altyapısı alır.|  
|[IDebugDocumentHelper::CreateDebugDocumentContext](../../winscript/reference/idebugdocumenthelper-createdebugdocumentcontext.md)|Yeni bir hata ayıklama belge bağlam oluşturur.|  
|[IDebugDocumentHelper::BringDocumentToTop](../../winscript/reference/idebugdocumenthelper-bringdocumenttotop.md)|Bu belge üst hata ayıklayıcı kullanıcı arabirimi sunar.|  
|[IDebugDocumentHelper::BringDocumentContextToTop](../../winscript/reference/idebugdocumenthelper-bringdocumentcontexttotop.md)|Bu belge bağlamında hata ayıklayıcı kullanıcı arabiriminin en üstüne getirir.|