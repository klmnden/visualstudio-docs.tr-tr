---
title: Iremotedebugapplication arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IRemoteDebugApplication interface
ms.assetid: 96bf2a3f-049f-46ba-86ad-57fc184343a2
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 02ddf409bf25cb86fc742cdc004e2f1b664d22e3
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54348769"
---
# <a name="iremotedebugapplication-interface"></a>IRemoteDebugApplication Arabirimi
Çalışan bir uygulamayı temsil eder. Bir işletim sistemi işlemine karşılık olarak gerekmez. Genellikle, bir hata ayıklayıcı hata ayıklama için bir uygulama hedefler. Hata ayıklama işlemi Yöneticisi eleman genellikle uygular.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IRemoteDebugApplication` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IRemoteDebugApplication::ResumeFromBreakPoint](../../winscript/reference/iremotedebugapplication-resumefrombreakpoint.md)|Bir kesme noktasına şu anda bir uygulama devam eder.|  
|[IRemoteDebugApplication::CauseBreak](../../winscript/reference/iremotedebugapplication-causebreak.md)|Uygulamanın ilk fırsatta hata ayıklayıcısına çalışmamasına neden olur.|  
|[IRemoteDebugApplication::ConnectDebugger](../../winscript/reference/iremotedebugapplication-connectdebugger.md)|Bir hata ayıklayıcı bu uygulamaya bağlanır.|  
|[IRemoteDebugApplication::DisconnectDebugger](../../winscript/reference/iremotedebugapplication-disconnectdebugger.md)|Geçerli hata ayıklayıcı uygulamadan bağlantısını keser.|  
|[IRemoteDebugApplication::GetDebugger](../../winscript/reference/iremotedebugapplication-getdebugger.md)|Geçerli hata ayıklayıcı uygulamaya bağlı döndürür.|  
|[IRemoteDebugApplication::CreateInstanceAtApplication](../../winscript/reference/iremotedebugapplication-createinstanceatapplication.md)|Hata ayıklayıcının IDE, çalışan giden işlem uygulama işleminde nesneleri oluşturmak için uygulama için bir mekanizma sağlar.|  
|[IRemoteDebugApplication::QueryAlive](../../winscript/reference/iremotedebugapplication-queryalive.md)|Uygulama duyarlı olup olmadığını gösterir.|  
|[IRemoteDebugApplication::EnumThreads](../../winscript/reference/iremotedebugapplication-enumthreads.md)|Uygulama ile ilişkili olduğu bilinen tüm iş parçacıklarının numaralandırır.|  
|[IRemoteDebugApplication::GetName](../../winscript/reference/iremotedebugapplication-getname.md)|Bu uygulama düğümü adını döndürür.|  
|[IRemoteDebugApplication::GetRootNode](../../winscript/reference/iremotedebugapplication-getrootnode.md)|Uygulamayla ilişkili tüm düğümleri eklendiği uygulama düğümü döndürür.|  
|[IRemoteDebugApplication::EnumGlobalExpressionContexts](../../winscript/reference/iremotedebugapplication-enumglobalexpressioncontexts.md)|Bu uygulama içinde çalışan tüm diller için genel ifade bağlamları numaralandırır.|