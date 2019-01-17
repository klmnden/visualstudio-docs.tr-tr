---
title: IWebAppDiagnosticsSetup::DiagnosticsSupported | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IWebAppDiagnosticsSetup::DiagnosticsSupported
ms.assetid: 5bbcd0d0-1460-4cf7-bbb1-f4f4a04f739a
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: df9296ac251d93105229fc0af365f6797a413f2b
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54349692"
---
# <a name="iwebappdiagnosticssetupdiagnosticssupported"></a>IWebAppDiagnosticsSetup::DiagnosticsSupported
Bu uygulamayı tanılama desteklenip desteklenmediğini belirler. Varsa [SetSite](http://go.microsoft.com/fwlink/?LinkId=232439) boş olmayan bir değer ile bu arabirimi uygulayan nesne çağrıldıktan [DiagnosticsSupported](../../winscript/reference/iwebappdiagnosticssetup-diagnosticssupported.md) döndürür `true`. Değilse, bunu döndürürse `false` ve çağrılar [IWebAppDiagnosticsSetup::CreateObjectWithSiteAtWebApp](../../winscript/reference/iwebappdiagnosticssetup-createobjectwithsiteatwebapp.md) başarısız.  
  
> [!IMPORTANT]
>  [Iwebappdiagnosticssetup arabirimi](../../winscript/reference/iwebappdiagnosticssetup-interface.md) PDM v11.0 tarafından uygulanan ve büyük. Activdbg100 içinde bulunamadı.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT DiagnosticsSupported(        [out, retval] VARIANT_BOOL* pRetVal        );  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 Varsa [SetSite](http://go.microsoft.com/fwlink/?LinkId=232439) boş olmayan bir değer ile bu arabirimi uygulayan nesne çağrıldıktan [DiagnosticsSupported](../../winscript/reference/iwebappdiagnosticssetup-diagnosticssupported.md) döndürür `true`. Değilse, bunu döndürürse `false`ve çağrılar [IWebAppDiagnosticsSetup::CreateObjectWithSiteAtWebApp](../../winscript/reference/iwebappdiagnosticssetup-createobjectwithsiteatwebapp.md) başarısız.