---
title: IWebAppDiagnosticsSetup::DiagnosticsSupported | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: 1d4214dea16c1e8a96ece7428f9ea73640025a9c
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63443678"
---
# <a name="iwebappdiagnosticssetupdiagnosticssupported"></a>IWebAppDiagnosticsSetup::DiagnosticsSupported
Bu uygulamayı tanılama desteklenip desteklenmediğini belirler. Varsa [SetSite](http://go.microsoft.com/fwlink/?LinkId=232439) boş olmayan bir değer ile bu arabirimi uygulayan nesne çağrıldıktan [DiagnosticsSupported](../../winscript/reference/iwebappdiagnosticssetup-diagnosticssupported.md) döndürür `true`. Değilse, bunu döndürürse `false` ve çağrılar [IWebAppDiagnosticsSetup::CreateObjectWithSiteAtWebApp](../../winscript/reference/iwebappdiagnosticssetup-createobjectwithsiteatwebapp.md) başarısız.  
  
> [!IMPORTANT]
> [Iwebappdiagnosticssetup arabirimi](../../winscript/reference/iwebappdiagnosticssetup-interface.md) PDM v11.0 tarafından uygulanan ve büyük. Activdbg100 içinde bulunamadı.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT DiagnosticsSupported(        [out, retval] VARIANT_BOOL* pRetVal        );  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 Varsa [SetSite](http://go.microsoft.com/fwlink/?LinkId=232439) boş olmayan bir değer ile bu arabirimi uygulayan nesne çağrıldıktan [DiagnosticsSupported](../../winscript/reference/iwebappdiagnosticssetup-diagnosticssupported.md) döndürür `true`. Değilse, bunu döndürürse `false`ve çağrılar [IWebAppDiagnosticsSetup::CreateObjectWithSiteAtWebApp](../../winscript/reference/iwebappdiagnosticssetup-createobjectwithsiteatwebapp.md) başarısız.