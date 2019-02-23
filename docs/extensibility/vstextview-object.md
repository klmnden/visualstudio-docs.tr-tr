---
title: VSTextView nesnesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- VSTextView
helpviewer_keywords:
- VSTextView object, reference
- views [Visual Studio SDK], reference
ms.assetid: 78272ddc-9718-4c65-a94e-a44a2e8d54f4
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ab54fce0271438f89ec66b4fc5d8db1ebe21634f
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56721426"
---
# <a name="vstextview-object"></a>VSTextView nesnesi
Metin görünümünü görüntülemek ve metin arabelleğini Unicode metni düzenlemek kullanıcıların olanak sağlayan bir penceredir. Esas olarak, hangi kullanıcıların çoğu düzenleyici olarak başvurmak görünümüdür. Görünüm arabellekteki çeşitli metin katmanları (sözcük kaydırma, anahat oluşturma metin ve benzeri) ayrılmış olduğundan, görünüm arabellekteki metni tam bir temsilini olmasını garanti edilmez. Metin görünümü hakkında daha fazla bilgi için bkz. [erişimcisinde görünümü eski API'yi kullanarak erişme](../extensibility/accessing-thetext-view-by-using-the-legacy-api.md)

 Aşağıdaki tabloda, arabirimler gösterilir <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView> nesne.

|Arabirim|Açıklama|
|---------------|-----------------|
|[IDropSource](/windows/desktop/api/oleidl/nn-oleidl-idropsource)|Standart OLE arabirimidir.|
|<xref:Microsoft.VisualStudio.OLE.Interop.IDropTarget>|Standart OLE arabirimidir.|
|<xref:Microsoft.VisualStudio.OLE.Interop.IObjectWithSite>|Standart OLE arabirimidir.|
|<xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget>|Standart OLE arabirimidir.|
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsCompoundAction>|Bileşik eylemleri (diğer bir deyişle, bir tek geri al/Yinele biriminde gruplandırılır eylemleri) oluşturulmasını sağlar.|
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView>|Temel yöntemleri, yönetme ve görüntüleme erişim sağlar. `IVsTextView` Güvenli iş parçacığına sahip değil.|
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane>|Oluşturur ve bir pencere bölmesi yönetir.|
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsLayeredTextView>|Metin katmanları ile etkileşim kurar.|
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsThreadSafeTextView>|Farklı bir iş parçacığından görünümü işlemleri gerçekleştirir.|

## <a name="see-also"></a>Ayrıca bkz.
- [Şekil Düzenle](https://www.microsoft.com/download/details.aspx?id=55984)
- [VSTextBuffer nesnesi](../extensibility/vstextbuffer-object.md)
- [Eski API'yi kullanarak erişen erişimcisinde görüntüle](../extensibility/accessing-thetext-view-by-using-the-legacy-api.md)