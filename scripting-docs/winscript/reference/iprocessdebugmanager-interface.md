---
title: Iprocessdebugmanager arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 5feb67b1a616eeaa855b27cb12ea9b3146545ebd
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54345129"
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