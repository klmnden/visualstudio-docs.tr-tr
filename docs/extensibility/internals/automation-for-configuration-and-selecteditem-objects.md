---
title: Yapılandırma ve SelectedItem nesneleri için Otomasyon | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- automation [Visual Studio SDK], SelectedItem object
- automation [Visual Studio SDK], builds
ms.assetid: 120377f1-51aa-4445-b2f7-06ab7fc2b47f
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e6c9dc8012433f9ec73f15b9249f6b7ac08bdad7
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66347968"
---
# <a name="automation-for-configuration-and-selecteditem-objects"></a>Yapılandırma ve SelectedItem nesneleri için Otomasyon

Yapı ve Visual Studio seçili öğe işlemleri otomatik hale getirebilirsiniz.

## <a name="automation-for-builds"></a>Yapılar için Otomasyon

Derleme veya yapılandırma, uyguladığınızda sağlanan bir otomasyon modeli olan <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProvider>. Daha fazla bilgi için [anlayın derleme yapılandırmaları](../../ide/understanding-build-configurations.md).

VSPackage'ı oluşturma ve yapılandırma seçeneklerini denetlemek isterseniz, otomasyon modeli kullanmanız gerekir.

## <a name="automation-for-selecteditem"></a>SelectedItem için Otomasyon

Bir uygulama için sağlaması gerekmez `SelectedItem` Visual Studio standart uygulaması içerdiğinden nesne. Ancak, uygulayabileceğiniz `SelectedItem` tercih ederseniz nesne. İçeren bir nesne uygulamalıdır `SelectedItem` arabirim ve çağrısı için bir yanıt döndüreceğini <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetPropertyPage%2A> yöntemiyle `VSITEMID` kümesine [__VSHPROPID. VSHPROPID_ExtSelectedItem](<xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID.VSHPROPID_ExtSelectedItem>).

## <a name="see-also"></a>Ayrıca bkz.

- <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetPropertyPage%2A>
- [Otomasyon modeline katkıda bulunma](../../extensibility/internals/contributing-to-the-automation-model.md)
- [Derleme yapılandırmalarını anlama](../../ide/understanding-build-configurations.md)