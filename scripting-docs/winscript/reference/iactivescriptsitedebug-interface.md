---
title: Iactivescriptsitedebug arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptSiteDebug interface
ms.assetid: 2557ee09-688b-4c03-a821-180c24dfa0e6
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 339325686d2a98e34c6e9f96056612769a9e110e
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54348314"
---
# <a name="iactivescriptsitedebug-interface"></a>IActiveScriptSiteDebug Arabirimi
Akıllı ana uygulama `IActiveScriptSiteDebug` belge yönetimi gerçekleştirmek ve hata ayıklamaya katılmak için arabirim. `IActiveScriptSite` Nesne, genellikle uygulanmasını sağlar `IActiveScriptSiteDebug` arabirimi. Bu yapıldığında çağrı `IActiveScriptSite::QueryInterface` elde etmek için yöntemi `IActiveScriptSiteDebug` arabirimi.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IActiveScriptSiteDebug` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IActiveScriptSiteDebug::GetDocumentContextFromPosition](../../winscript/reference/iactivescriptsitedebug-getdocumentcontextfromposition.md)|Temsilci seçme için dil altyapısı tarafından kullanılan `IDebugCodeContext::GetSourceContext`.|  
|[IActiveScriptSiteDebug::GetApplication](../../winscript/reference/iactivescriptsitedebug-getapplication.md)|Bu betik sitesiyle ilişkili hata ayıklama uygulama nesnesi döndürür.|  
|[IActiveScriptSiteDebug::GetRootApplicationNode](../../winscript/reference/iactivescriptsitedebug-getrootapplicationnode.md)|Altında hangi betiği belgelerin eklenmesi gereken uygulama düğümünü alır.|  
|[IActiveScriptSiteDebug::OnScriptErrorDebug](../../winscript/reference/iactivescriptsitedebug-onscripterrordebug.md)|Çalışma zamanı hatalarının nasıl işleneceğini belirlemek bir akıllı ana bilgisayar sağlar.|