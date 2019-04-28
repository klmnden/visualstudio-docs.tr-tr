---
title: Idebugdocumenttextevents arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugDocumentTextEvents interface
ms.assetid: 341b20fd-994c-4030-a06b-6c66ad38c35d
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7c83a6e3a41ed7087338989d5cb077fa070e724b
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63434259"
---
# <a name="idebugdocumenttextevents-interface"></a>IDebugDocumentTextEvents Arabirimi
İlişkili metin belgeye yapılan değişiklikler belirten olayları sağlar.  
  
> [!NOTE]
> Ateş olayları bu arabirim, belge metnini değiştirir. Olay işleyicileri almak kullanarak yeni metin `IDebugDocumentText` arabirimi.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IDebugDocumentTextEvents` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugDocumentTextEvents::onDestroy](../../winscript/reference/idebugdocumenttextevents-ondestroy.md)|Temel alınan belge yok edildi ve artık geçerli değil gösterir|  
|[IDebugDocumentTextEvents::onInsertText](../../winscript/reference/idebugdocumenttextevents-oninserttext.md)|Belgeye yeni bir metin eklendiğini gösterir|  
|[IDebugDocumentTextEvents::onRemoveText](../../winscript/reference/idebugdocumenttextevents-onremovetext.md)|Metin belgesinden kaldırıldığını gösterir.|  
|[IDebugDocumentTextEvents::onReplaceText](../../winscript/reference/idebugdocumenttextevents-onreplacetext.md)|Metin değiştirildiğini gösterir.|  
|[IDebugDocumentTextEvents::onUpdateTextAttributes](../../winscript/reference/idebugdocumenttextevents-onupdatetextattributes.md)|Temel karakter konumu aralığı ile ilişkili metin öznitelikleri değiştiğini gösterir.|  
|[IDebugDocumentTextEvents::onUpdateDocumentAttributes](../../winscript/reference/idebugdocumenttextevents-onupdatedocumentattributes.md)|Belgenin özniteliklerini değiştiğini gösterir.|