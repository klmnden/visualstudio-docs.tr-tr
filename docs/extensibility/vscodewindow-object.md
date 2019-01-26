---
title: VSCodeWindow nesnesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- VSCodeWindow
helpviewer_keywords:
- views [Visual Studio SDK], VSCodeWindow object
- VsCodeWindow object
ms.assetid: cf5fe926-e784-4098-bc01-cac49c7c55c6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e674077ba3b26ea4b0cbc3bf19e2f526e381f72d
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54959794"
---
# <a name="vscodewindow-object"></a>VSCodeWindow nesnesi
Bir veya daha fazla metin görünümleri genellikle içerebilir bir özel belge penceresi bir kod penceredir <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView> nesne.  
  
 Bu mimari, kod penceresi bir pencere çerçevesinde bir belge penceresi ' dir. İşlevsel olarak, kod penceresi ek özelliklere sahip bir belge penceresi yalnızca ' dir. Çok Belgeli Arabirim (MDI) modunda kod penceresinde MDI alt çerçeve ' dir. Daha fazla bilgi için [eski API'sini kullanarak kod windows özelleştirme](../extensibility/customizing-code-windows-by-using-the-legacy-api.md).  
  
 Aşağıdaki tablo, arabirimlerini içerir <xref:Microsoft.VisualStudio.TextManager.Interop.VsCodeWindow> nesne.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|<xref:Microsoft.VisualStudio.OLE.Interop.IServiceProvider>|Bir genel benzersiz tanıtıcısı (GUID) tanımlayan bir hizmet bulmak için bir genel erişim mekanizması sağlar.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindow>|Bir veya daha fazla kod görünümleri içeren birden çok belge arabirimi (MDI) alt temsil eder.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane>|Pencere çerçevesi doldurur.|  
  
## <a name="see-also"></a>Ayrıca bkz.  
 <xref:Microsoft.VisualStudio.OLE.Interop.IServiceProvider>   
 [Şekil Düzenle](https://www.microsoft.com/download/details.aspx?id=55984)