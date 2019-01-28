---
title: VSTextView nesnesi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- VSTextView
helpviewer_keywords:
- VSTextView object, reference
- views [Visual Studio SDK], reference
ms.assetid: 78272ddc-9718-4c65-a94e-a44a2e8d54f4
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: e8ed14761b77e3469b2c19d0e9fd2ff3732bb72d
ms.sourcegitcommit: 447f2174bdecdd471d8a8e11c19554977db620a0
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/28/2019
ms.locfileid: "55089233"
---
# <a name="vstextview-object"></a>VSTextView Nesnesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Metin görünümünü görüntülemek ve metin arabelleğini Unicode metni düzenlemek kullanıcılara bir penceredir. Esas olarak, hangi kullanıcıların çoğu düzenleyici olarak başvurmak görünümüdür. Görünüm arabellekteki çeşitli metin katmanları (sözcük kaydırma, anahat oluşturma metin ve benzeri) ayrılmış olduğundan, görünüm arabellekteki metni tam bir temsilini olmasını garanti edilmez. Metin görünümü hakkında daha fazla bilgi için bkz. [erişimcisinde görünümü eski API'yi kullanarak erişme](../extensibility/accessing-thetext-view-by-using-the-legacy-api.md)  
  
 Aşağıdaki tabloda, arabirimler gösterilir <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView> nesne.  
  
|Arabirim|Açıklama|  
|---------------|-----------------|  
|[IDropSource](/windows/desktop/api/oleidl/nn-oleidl-idropsource)|Standart OLE arabirimidir.|  
|<xref:Microsoft.VisualStudio.OLE.Interop.IDropTarget>|Standart OLE arabirimidir.|  
|<xref:Microsoft.VisualStudio.OLE.Interop.IObjectWithSite>|Standart OLE arabirimidir.|  
|<xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget>|Standart OLE arabirimidir.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsCompoundAction>|Bileşik eylemleri (diğer bir deyişle, bir tek geri al/Yinele biriminde gruplandırılır eylemleri) oluşturulmasını sağlar.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView>|Temel yöntemleri, yönetme ve görüntüleme erişim sağlar. `IVsTextView` iş parçacığı güvenli değildir.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane>|Oluşturur ve bir pencere bölmesi yönetir.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsLayeredTextView>|Metin katmanları ile etkileşim kurar.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsThreadSafeTextView>|Farklı bir iş parçacığından görünümü işlemleri gerçekleştirir.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Şekil Düzenle](http://msdn.microsoft.com/f08872bd-fd9c-4e36-8cf2-a2a2622ef986)   
 [VSTextBuffer Object](../extensibility/vstextbuffer-object.md)   
 [Eski API'yi Kullanarak Metin Görünümüne Erişme](../extensibility/accessing-thetext-view-by-using-the-legacy-api.md)
