---
title: Iprocessdebugmanager arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IProcessDebugManager interface
ms.assetid: b6ecb2bd-a4d1-4857-9232-036c154d0cb1
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d68c044cdc3d523841cc56814b8ca34bcd8aa037
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58157249"
---
# <a name="iprocessdebugmanager-interface"></a>IProcessDebugManager Arabirimi
İşlem Hata Ayıklama Yöneticisi birincil arabirim. Bu arabirim, oluşturma, ekleme veya bir sanal uygulama bir işlemden kaldırma. Yığın çerçeveleri ve uygulama iş parçacığı sıralayabilirsiniz.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IProcessDebugManager` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IProcessDebugManager::CreateApplication](../../winscript/reference/iprocessdebugmanager-createapplication.md)|Bu uygulama için yeni bir hata ayıklama uygulama nesnesi oluşturur.|  
|[IProcessDebugManager::GetDefaultApplication](../../winscript/reference/iprocessdebugmanager-getdefaultapplication.md)|Geçerli işlem için bir varsayılan uygulama nesnesi döndürür.|  
|[IProcessDebugManager::AddApplication](../../winscript/reference/iprocessdebugmanager-addapplication.md)|Çalışan uygulamalar bir uygulama makinesi ayıklama manager'ın listesine ekler.|  
|[IProcessDebugManager::RemoveApplication](../../winscript/reference/iprocessdebugmanager-removeapplication.md)|Bir uygulamanın çalışmasını kaldırır uygulama listesi.|  
|[IProcessDebugManager::CreateDebugDocumentHelper](../../winscript/reference/iprocessdebugmanager-createdebugdocumenthelper.md)|Bu uygulama için yeni bir hata ayıklama belge Yardımcısı oluşturur.|