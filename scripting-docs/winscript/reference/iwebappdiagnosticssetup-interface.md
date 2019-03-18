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
ms.openlocfilehash: b84fd126ebd4d311264efa5d2156f9d83961fee9
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58148756"
---
# <a name="iwebappdiagnosticssetup-interface"></a>IWebAppDiagnosticsSetup Arabirimi
Bu arabirim PDM hata ayıklama uygulama ayıklanmakta olan işlemde COM nesneleri oluşturma ve web tanılamayı etkinleştirmeyi tarafından uygulanır. Uygulama nesnesi uygulayan PDM hatalarını ayıklıyorsanız [IObjectWithSite](http://go.microsoft.com/fwlink/?LinkId=232438), Internet Explorer'ı çağırır [SetSite](http://go.microsoft.com/fwlink/?LinkId=232439) oluşturulduktan sonra ve bir başvuru geçirir [Iwebbrowser2](http://go.microsoft.com/fwlink/?LinkId=232449). WWA uygulama çağrıları [SetSite](http://go.microsoft.com/fwlink/?LinkId=232439) ve WWA geçişlerinde IWebApplicationHost bunun yerine arabirimi. Varsa [SetSite](http://go.microsoft.com/fwlink/?LinkId=232439) NULL olmayan bir değer ile çağırıldı [IWebAppDiagnosticsSetup::DiagnosticsSupported](../../winscript/reference/iwebappdiagnosticssetup-diagnosticssupported.md) true değerini döndürür. Değilse, false değerini döndürür ve çağrılar [IWebAppDiagnosticsSetup::CreateObjectWithSiteAtWebApp](../../winscript/reference/iwebappdiagnosticssetup-createobjectwithsiteatwebapp.md) başarısız.  
  
> [!IMPORTANT]
>  `IWebAppDiagnosticsSetup` PDM v11.0 ve büyük uygulanır. activdbg100.h içinde bulunur.  
  
## <a name="methods"></a>Yöntemler  
 Bu arabirim, aşağıdaki yöntemi kullanıma sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IWebAppDiagnosticsSetup::CreateObjectWithSiteAtWebApp](../../winscript/reference/iwebappdiagnosticssetup-createobjectwithsiteatwebapp.md)|Belirtilen filtre tarafından gizlenen metin belgeleri alır.|  
|[IWebAppDiagnosticsSetup::DiagnosticsSupported](../../winscript/reference/iwebappdiagnosticssetup-diagnosticssupported.md)|Belirtilen belge bu düğümün alt düğümleri birine ait olup olmadığını belirler.|