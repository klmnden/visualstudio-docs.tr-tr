---
title: IWebAppDiagnosticsSetup::CreateObjectWithSiteAtWebApp | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IWebAppDiagnosticsSetup::CreateObjectWithSiteAtWebApp
ms.assetid: 30975973-acb1-48f4-8266-5e097a57db22
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 26403a168268e817644637544d64d4205c398b75
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58157665"
---
# <a name="iwebappdiagnosticssetupcreateobjectwithsiteatwebapp"></a>IWebAppDiagnosticsSetup::CreateObjectWithSiteAtWebApp
Bu yöntem birlikte kimliği ile geçirdiğiniz sınıfı oluşturur `rclsid` kullanarak `dwClsContext`. Bu şekilde benzer [IRemoteDebugApplication::CreateInstanceAtApplication](../../winscript/reference/iremotedebugapplication-createinstanceatapplication.md) durumunda hariç çalıştığı `CreateObjectWithSiteAtWebApp` nesne web uygulamasının kullanıcı Arabirimi iş parçacığında zaman uyumsuz olarak oluşturulur. Sınıf kimliği tarafından belirtilen nesnede uygulamalıdır [Iwebappdiagnosticsobjectınitialization arabirimi](../../winscript/reference/iwebappdiagnosticsobjectinitialization-interface.md). Nesne oluşturulduktan sonra [IWebAppDiagnosticsObjectInitialization::Initialize](../../winscript/reference/iwebappdiagnosticsobjectinitialization-initialize.md) PDM hata ayıklama uygulama başvurusuyla çağrılır ve `hPassToObject` parametresinin `CreateObjectWithSiteAtWebApp`. Uygulamaya bir tanıtıcı kullanarak kopyaladığınız anonim bir kanala geçirmek için bu yöntemi kullanabilirsiniz [DuplicateHandle](http://go.microsoft.com/fwlink/?LinkId=232450).  
  
> [!IMPORTANT]
>  [Iwebappdiagnosticssetup arabirimi](../../winscript/reference/iwebappdiagnosticssetup-interface.md) PDM v11.0 tarafından uygulanan ve büyük. activdbg100.h içinde bulunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT CreateObjectWithSiteAtWebApp(        [in] REFCLSID rclsid,         [in] DWORD dwClsContext,         [in] REFIID riid,         [in] DWORD_PTR hPassToObject        );  
```  
  
#### <a name="parameters"></a>Parametreler  
 `rclsid`  
 Sınıf kimliği oluşturma sınıf.  
  
 `dwClsContext`  
 Kod çalıştırılacağı bağlamı. Çoğu durumda bu CLSCTX_INPROC_SERVER olur.  
  
 `riid`  
 Kullanılmadı.  
  
 `hPassToObject`  
 UI iş parçacığı üzerinde oluşturulduktan sonra nesne uygulayan nesnesine geçirilen bir değeri [Iwebappdiagnosticsobjectınitialization arabirimi](../../winscript/reference/iwebappdiagnosticsobjectinitialization-interface.md).