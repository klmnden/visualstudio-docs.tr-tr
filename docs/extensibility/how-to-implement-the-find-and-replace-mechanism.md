---
title: 'Nasıl yapılır: Uygulama Bul ve Değiştir mekanizması | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - find and replace
ms.assetid: bbd348db-3d19-42eb-99a2-3e808528c0ca
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9d803e074970e2827f7e644d29d12e4df920d7c4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62862972"
---
# <a name="how-to-implement-the-find-and-replace-mechanism"></a>Nasıl yapılır: Bul uygulamak ve mekanizmasını değiştirin

Visual Studio Bul/Değiştir kullanmanın iki yolu sağlar. Bir metin resim kabuğa geçirin ve, arama, vurgulama ve değiştirmeyi metin işlemek yoludur. Bu, kullanıcıların birden çok metin yayılma belirtmesine izin verir. Alternatif olarak, bu işlev, VSPackage'ı kontrol edebilirsiniz. Her iki durumda da geçerli hedef ve bütün açık belgeleri hedeflerini hakkında Kabuk bildirmeniz gerekir.

## <a name="to-implement-findreplace"></a>Bul/Değiştir uygulamak için

1. Uygulama <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget> çerçeve özellikleri tarafından döndürülen nesne bir arabirimdeki <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID.VSFPROPID_DocView> veya <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID.VSFPROPID_DocData>. Özel bir düzenleyici oluşturuyorsanız, özel düzenleyici sınıfı bir parçası olarak bu arabirimi uygulamalıdır.

2. Kullanım <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.GetCapabilities%2A> düzenleyiciniz destekleyen seçenekleri belirtin ve metin, görüntü arama uygulayıp uygulamadığını belirtmek için yöntemi.

   Düzenleyici metin, görüntü arama destekliyorsa, uygulama <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.GetSearchImage%2A>.

   Aksi takdirde uygulama <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Find%2A> ve <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Replace%2A>.

3. Uygularsanız <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Find%2A> ve <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Replace%2A> yöntemleri çağırarak arama görevlerinizi basitleştirebilecek <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindHelper> arabirimi.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindHelper>
- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget>
- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Find%2A>
- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.GetSearchImage%2A>
- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Replace%2A>
- <xref:Microsoft.VisualStudio.Shell.Interop.__VSPROPID>