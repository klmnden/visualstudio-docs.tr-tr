---
title: Idebugdocumenthost arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugDocumentHost interface
ms.assetid: 2fed4220-b6a2-47c6-bf28-daad7dd5c42d
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 46684bf2264813a8daaa466b98119496ba85d4b9
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54346546"
---
# <a name="idebugdocumenthost-interface"></a>IDebugDocumentHost Arabirimi
Sözdizimi renklendirme, hata ayıklayıcıya gibi ana bilgisayara özgü işlevleri kullanıma sunar. `IDebugDocumentHelper::SetDebugDocumentHost` Yöntemi bu arabirimi bağımsız değişken olarak alır.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IDebugDocumentHost` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugDocumentHost::GetDeferredText](../../winscript/reference/idebugdocumenthost-getdeferredtext.md)|Kullanılarak eklenmiş olan karakter aralığı döndürür `IDebugDocumentHelper::AddDeferredText`, özgün ana bilgisayar belgedeki.|  
|[IDebugDocumentHost::GetScriptTextAttributes](../../winscript/reference/idebugdocumenthost-getscripttextattributes.md)|Belge metin bloğu için metin öznitelikleri döndürür.|  
|[IDebugDocumentHost::OnCreateDocumentContext](../../winscript/reference/idebugdocumenthost-oncreatedocumentcontext.md)|Konağın, yeni bir belge bağlamına oluşturulmakta olduğundan ve isteğe bağlı olarak yeni bir bağlam denetleyen nesneyi döndürmek üzere konak sağlar bildirir.|  
|[IDebugDocumentHost::GetPathName](../../winscript/reference/idebugdocumenthost-getpathname.md)|Belgenin kaynak dosyasının tam yolu (dosya adı dahil) döndürür.|  
|[IDebugDocumentHost::GetFileName](../../winscript/reference/idebugdocumenthost-getfilename.md)|Yol bilgisi olmadan belgenin adını döndürür.|  
|[IDebugDocumentHost::NotifyChanged](../../winscript/reference/idebugdocumenthost-notifychanged.md)|Konak, belgenin kaynak dosya kaydedildi ve içeriğini yenileneceğini bildirir.|