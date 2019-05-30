---
title: İç içe projeler için addItem iletişim kutusunu filtreleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- filtering, nested projects
- nested projects, AddItem dialog box filtering
ms.assetid: 5b3e352e-7f18-4f66-be16-b0ad55637ce5
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: bc3ff1f85e8c8c71bf8ef16e6fe0c89bf3613f4d
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66328958"
---
# <a name="filter-the-additem-dialog-box-for-nested-projects"></a>İç içe projeler için addItem iletişim kutusunu filtreleme
Görüntülerken bir **addItem** ana proje iç içe geçmiş proje için iletişim kutusu, hangi öğeleri iletişim kutusunda görüntülenen denetleyebilirsiniz.

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFilterAddProjectItemDlg2> Arabirimi sayesinde filtre olacak düğümleri bir **addItem** iletişim kutusu. Alt projenin görüntülendiğinde **addItem** iletişim kutusu, üst uygulayabilirsiniz `IVsFilterAddProjectItemDlg` çocuğun projesinde gösterilecek arabirimi ve filtre öğeleri.

 Projeleri, belirli bir üst projeleri altında işlevi tarafından gruplandırıldığında, uygulayabileceğiniz `IVsFilterAddProjectItemDlg` kullanıcı seçtiğinde **proje Öğe Ekle** iç içe geçmiş bir projedeki kısayol menüsünde. Uygulama `IvsFilterAddProjectItemDlg displays` yalnızca proje öğelerini ya da bu gruba belirli dosyaları. Aynı dizinde depolanan bile diğer gruplar için proje öğeleri iletişim kutusu dışı filtrelenir.

 Kullanıcı açtığında **addItem** alt, üst projenin uygulaması için iletişim kutusu `IVsFilterAddProjectItemDlg` arabirimi çağrılır.

 `IVsFilterAddProjectItemDlg` Arabirimi, kategoriye göre filtreleme de uygulayabilirsiniz. Daha fazla bilgi için [Yeni Öğe Ekle iletişim kutusuna öğeleri ekleme](../../extensibility/internals/adding-items-to-the-add-new-item-dialog-boxes.md) ve [proje ve öğe şablonlarını kaydetme](../../extensibility/internals/registering-project-and-item-templates.md).

## <a name="see-also"></a>Ayrıca bkz.
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsFilterAddProjectItemDlg2>
- [Yeni Öğe Ekle iletişim kutusu öğeleri Ekle](../../extensibility/internals/adding-items-to-the-add-new-item-dialog-boxes.md)
- [Proje ve öğe şablonlarını kaydetme](../../extensibility/internals/registering-project-and-item-templates.md)
- [İç içe projeler](../../extensibility/internals/nesting-projects.md)