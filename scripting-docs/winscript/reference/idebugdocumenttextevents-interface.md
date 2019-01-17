---
title: Idebugdocumenttextevents arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: bec89ae81d79fb7b0d822cafe2bf44f0ecd8ad81
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54345667"
---
# <a name="idebugdocumenttextevents-interface"></a>IDebugDocumentTextEvents Arabirimi
İlişkili metin belgeye yapılan değişiklikler belirten olayları sağlar.  
  
> [!NOTE]
>  Ateş olayları bu arabirim, belge metnini değiştirir. Olay işleyicileri almak kullanarak yeni metin `IDebugDocumentText` arabirimi.  
  
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