---
title: Iscriptnode arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IScriptNode interface
ms.assetid: cfa76c4a-6543-48e8-a946-d212cd0bf934
caps.latest.revision: 21
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d8897d783f8a101b41dd7263061604fb1d82ec56
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54344622"
---
# <a name="iscriptnode-interface"></a>IScriptNode Arabirimi
Uygulayan bir nesne `IScriptNode` arabirimi bir Web sayfasını temsil eder.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IScriptNode` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IScriptNode::Alive](../../winscript/reference/iscriptnode-alive.md)|Bir nesne hala etkin olup olmadığını belirtir.|  
|[Iscriptnode:: CreateChildEntry](../../winscript/reference/iscriptnode-createchildentry.md)|Bir alt örneğini ekler `IScriptEntry`.|  
|[IScriptNode::CreateChildHandler](../../winscript/reference/iscriptnode-createchildhandler.md)|Bir kod oluşturma ekler alt örnek olarak bir `IScriptNode`.|  
|[IScriptNode::Delete](../../winscript/reference/iscriptnode-delete.md)|Nesne ağacının siler.|  
|[IScriptNode::GetChild](../../winscript/reference/iscriptnode-getchild.md)|Belirtilen dizin düğümünde en alt öğesini döndürür.|  
|[IScriptNode::GetCookie](../../winscript/reference/iscriptnode-getcookie.md)|Bir kod oluşturma konak nesnesiyle ilişkilendirmek için kullanılan uygulama tanımlı bir değer döndürür.|  
|[IScriptNode::GetIndexInParent](../../winscript/reference/iscriptnode-getindexinparent.md)|Üst öğenin alt listedeki bir nesnenin dizinini döndürür.|  
|[IScriptNode::GetLanguage](../../winscript/reference/iscriptnode-getlanguage.md)|Geçerli betik düğümü tarafından kullanılan kodlama dilini döndürür.|  
|[IScriptNode::GetNumberOfChildren](../../winscript/reference/iscriptnode-getnumberofchildren.md)|Alt düğümleri sayısını döndürür `IScriptNode` nesne.|  
|[IScriptNode::GetParent](../../winscript/reference/iscriptnode-getparent.md)|Döndürür `IScriptNode` bir nesnenin üst nesnesi.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Yazma Arabirimleri](../../winscript/reference/active-script-authoring-interfaces.md)