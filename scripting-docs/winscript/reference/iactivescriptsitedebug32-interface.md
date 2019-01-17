---
title: Iactivescriptsitedebug32 arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 03f42217-303d-46e7-9792-61a5ab95252c
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
ms.openlocfilehash: e7937311e01274570e34bd639a0dc5f68206a3aa
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54345571"
---
# <a name="iactivescriptsitedebug32-interface"></a>Iactivescriptsitedebug32 arabirimi
Akıllı ana uygulama `IActiveScriptSiteDebug32` belge yönetimi gerçekleştirmek ve hata ayıklamaya katılmak için arabirim. `IActiveScriptSite` Nesne, genellikle uygulanmasını sağlar `IActiveScriptSiteDebug32` arabirimi. Bu yapıldığında çağrı `IActiveScriptSite::QueryInterface` elde etmek için yöntemi `IActiveScriptSiteDebug32` arabirimi.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IActiveScriptSiteDebug32` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IActiveScriptSiteDebug32::GetApplication](../../winscript/reference/iactivescriptsitedebug32-getapplication.md)|Bu betik sitesiyle ilişkili hata ayıklama uygulama nesnesi döndürür.|  
|[IActiveScriptSiteDebug32::GetDocumentContextFromPosition](../../winscript/reference/iactivescriptsitedebug32-getdocumentcontextfromposition.md)|Temsilci seçme için dil altyapısı tarafından kullanılan `IDebugCodeContext::GetSourceContext`.|