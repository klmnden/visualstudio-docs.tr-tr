---
title: Iwebappdiagnosticssetup arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IWebAppDiagnosticsSetup Interface
ms.assetid: ec7359f2-633e-4d59-b64b-9cab0134dfd0
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 71d4501fff04b62abe392c6684a4a0551dea9ee8
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63443655"
---
# <a name="iwebappdiagnosticssetup-interface"></a>IWebAppDiagnosticsSetup Arabirimi
Bu arabirim PDM hata ayıklama uygulama ayıklanmakta olan işlemde COM nesneleri oluşturma ve web tanılamayı etkinleştirmeyi tarafından uygulanır. Uygulama nesnesi uygulayan PDM hatalarını ayıklıyorsanız [IObjectWithSite](http://go.microsoft.com/fwlink/?LinkId=232438), Internet Explorer'ı çağırır [SetSite](http://go.microsoft.com/fwlink/?LinkId=232439) oluşturulduktan sonra ve bir başvuru geçirir [Iwebbrowser2](http://go.microsoft.com/fwlink/?LinkId=232449). WWA uygulama çağrıları [SetSite](http://go.microsoft.com/fwlink/?LinkId=232439) ve WWA geçişlerinde IWebApplicationHost bunun yerine arabirimi. Varsa [SetSite](http://go.microsoft.com/fwlink/?LinkId=232439) NULL olmayan bir değer ile çağırıldı [IWebAppDiagnosticsSetup::DiagnosticsSupported](../../winscript/reference/iwebappdiagnosticssetup-diagnosticssupported.md) true değerini döndürür. Değilse, false değerini döndürür ve çağrılar [IWebAppDiagnosticsSetup::CreateObjectWithSiteAtWebApp](../../winscript/reference/iwebappdiagnosticssetup-createobjectwithsiteatwebapp.md) başarısız.  
  
> [!IMPORTANT]
> `IWebAppDiagnosticsSetup` PDM v11.0 ve büyük uygulanır. activdbg100.h içinde bulunur.  
  
## <a name="methods"></a>Yöntemler  
 Bu arabirim, aşağıdaki yöntemi kullanıma sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IWebAppDiagnosticsSetup::CreateObjectWithSiteAtWebApp](../../winscript/reference/iwebappdiagnosticssetup-createobjectwithsiteatwebapp.md)|Belirtilen filtre tarafından gizlenen metin belgeleri alır.|  
|[IWebAppDiagnosticsSetup::DiagnosticsSupported](../../winscript/reference/iwebappdiagnosticssetup-diagnosticssupported.md)|Belirtilen belge bu düğümün alt düğümleri birine ait olup olmadığını belirler.|