---
title: 'Nasıl yapılır: Windows için Otomasyon sağlar | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- automation [Visual Studio SDK], tool windows
- tool windows, automation
ms.assetid: 512ab2a4-7987-4912-8f40-8804bf66f829
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 7ea7b79df4e7f3748ec2bc7f5e57c6ecb7dfca5b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68191840"
---
# <a name="how-to-provide-automation-for-windows"></a>Nasıl yapılır: Windows için Otomasyon Sağlama
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Otomasyon için belge ve araç pencerelerini sağlayabilir. Görev listesi ile yaptığı gibi Otomasyon nesneleri bir penceresinde kullanılabilir hale getirmek istediğiniz ve ortam zaten bir hazır Otomasyon nesnesi sağlamaz sağlayarak Otomasyon daha önerilir.  
  
## <a name="automation-for-tool-windows"></a>Aracı Windows için Otomasyon  
 Araç penceresinde Otomasyon döndüren ve standart bir ortam sağlar <xref:EnvDTE.Window> nesne aşağıdaki yordamda açıklandığı gibi:  
  
#### <a name="to-provide-automation-for-tool-windows"></a>Araç pencereleri için Otomasyon sağlamak için  
  
1. Çağrı <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.GetProperty%2A> ortamıyla yöntemiyle <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID> olarak `VSFPROPID` almak için parametre `Window` nesne.  
  
2. Çağıran bir VSPackage özgü Otomasyon nesnesi için araç penceresi istediğinde <xref:EnvDTE.Window.Object%2A>, ortam çağrıları `QueryInterface` için `IExtensibleObject`, <xref:Microsoft.VisualStudio.Shell.Interop.IVsExtensibleObject>, veya `IDispatch` arabirimleri. Her ikisi de `IExtensibleObject` ve `IVsExtensibleObject` sağlayan bir <xref:Microsoft.VisualStudio.Shell.Interop.IVsExtensibleObject.GetAutomationObject%2A> yöntemi.  
  
3. Ortam sonra çağırdığında `GetAutomationObject` geçirme yöntemi `NULL`, geçirerek yanıt VSPackage özgü nesnenizin yedekleyin.  
  
4. Çağırma varsa `QueryInterface` için `IExtensibleObject` ve `IVsExtensibleObject` ortam çağırır, başarısız olursa `QueryInterface` için `IDispatch`.  
  
## <a name="automation-for-document-windows"></a>Belge Windows için Otomasyon  
 Standart <xref:EnvDTE.Document> nesne kullanılabilir ayrıca ortamından bir düzenleyici kendi uygulaması içerebilmesine karşın `T:EnvDTE.Document` uygulayarak nesne `IExtensibleObject` arabirimi ve yanıtlama `GetAutomationObject`.  
  
 Ayrıca, bir düzenleyici üzerinden alınan bir VSPackage özgü Otomasyon nesnesi sağlayabilirsiniz <xref:EnvDTE.Document.Object%2A> uygulayarak yöntemi `IVsExtensibleObject` veya `IExtensibleObject` arabirimleri. [VSSDK örnekleri](../../misc/vssdk-samples.md) bir RTF belgeye özgü Otomasyon nesnesi katkıda bulunur.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsExtensibleObject>
