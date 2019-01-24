---
title: VSCodeWindow nesnesi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- VSCodeWindow
helpviewer_keywords:
- views [Visual Studio SDK], VSCodeWindow object
- VsCodeWindow object
ms.assetid: cf5fe926-e784-4098-bc01-cac49c7c55c6
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 1711b1409e42d431ad34badf82cff68e5a9bad75
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54779298"
---
# <a name="vscodewindow-object"></a>VSCodeWindow Nesnesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir veya daha fazla metin görünümleri genellikle içerebilir bir özel belge penceresi bir kod penceredir <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView> nesne.  
  
 Bu mimari, kod penceresi bir pencere çerçevesinde bir belge penceresi ' dir. İşlevsel olarak, kod penceresi ek özelliklere sahip bir belge penceresi yalnızca ' dir. Çok Belgeli Arabirim (MDI) modunda kod penceresinde MDI alt çerçeve ' dir. Daha fazla bilgi için [eski API'yi kullanarak kod Windows özelleştirme](../extensibility/customizing-code-windows-by-using-the-legacy-api.md).  
  
 Aşağıdaki tablo, arabirimlerini içerir <xref:Microsoft.VisualStudio.TextManager.Interop.VsCodeWindow> nesne.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|<xref:Microsoft.VisualStudio.OLE.Interop.IServiceProvider>|Bir genel benzersiz tanıtıcısı (GUID) tanımlayan bir hizmet bulmak için bir genel erişim mekanizması sağlar.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindow>|Bir veya daha fazla kod görünümleri içeren birden çok belge arabirimi (MDI) alt temsil eder.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane>|Pencere çerçevesi doldurur.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.OLE.Interop.IServiceProvider>   
 [Şekil Düzenle](http://msdn.microsoft.com/f08872bd-fd9c-4e36-8cf2-a2a2622ef986)
