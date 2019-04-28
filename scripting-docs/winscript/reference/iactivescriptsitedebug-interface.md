---
title: Iactivescriptsitedebug arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: 3cd8043648586ed3c614cbb137e51d992d7ae29b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62992461"
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