---
title: Iremotedebugapplicationex arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IRemoteDebugApplicationEx Interface
ms.assetid: 8e16164d-dbb2-4488-9507-25ae34f343dc
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ab9e25a28ade1ac73b9e4837dae61e2d91f24c45
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58144413"
---
# <a name="iremotedebugapplicationex-interface"></a>IRemoteDebugApplicationEx Arabirimi
Çalışan bir uygulamayı temsil eder. Bir işletim sistemi işlemine karşılık olarak gerekmez. Genellikle, bir hata ayıklayıcı hata ayıklama için bir uygulama hedefler. Hata ayıklama işlemi Yöneticisi eleman genellikle uygular.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IRemoteDebugApplicationEx` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IRemoteDebugApplicationEx:GetHostPid](../../winscript/reference/iremotedebugapplicationex-gethostpid.md)|Konak uygulamanın işlem Kimliğini döndürür.|  
|GetHostMachineName|Konak uygulamanın üzerinde çalıştığı bilgisayarın adını döndürür.|  
|[IRemoteDebugApplicationEx:SetLocale](../../winscript/reference/iremotedebugapplicationex-setlocale.md)|Hata ayıklayıcı yerelleştirme dili ayarlar.|  
|[IRemoteDebugApplicationEx:ForceStepMode](../../winscript/reference/iremotedebugapplicationex-forcestepmode.md)|Tek adımlı modda hata ayıklayıcıya zorlar.|  
|[IRemoteDebugApplicationEx:RevokeBreak](../../winscript/reference/iremotedebugapplicationex-revokebreak.md)|Break komutunu iptal eder.|  
|SetProxyBlanketAndAddRef|Windows 95 tabanlı işletim sistemlerinden uzaktan hata ayıklama ile uyumluluğu sağlamak için hata ayıklayıcı nesne için bir proxy üzerinde COM güvenlik bilgilerini güncelleştirir.|  
|ReleaseFromSetProxyBlanket|Yayınları AddRef SetProxyBlanketAndAddRef öğesinden.|