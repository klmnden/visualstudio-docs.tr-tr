---
title: 'Nasıl yapılır: Yerleşik renklendirilebilir öğeleri kullanma | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- colorable items
- language services, built-in colorable items
ms.assetid: 5e5f3436-6bad-4fd2-8823-6a30353ba648
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e82b28a22d64ed1a97e2f932368da266b6b79d56
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56603059"
---
# <a name="how-to-use-built-in-colorable-items"></a>Nasıl yapılır: Yerleşik renklendirilebilir öğeleri kullanma
Yerleşik renklendirilebilir öğeleri kullanmadan önce öncelikle tümleşik geliştirme ortamı (IDE), bu durumda, kendi özel renklendirilebilir öğeler sağlamıyorsunuz sinyal gerekir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsProvideColorableItems> nesneleri. Dil hizmeti bir kayıt defteri anahtarını ayarlayarak bunu yapabilirsiniz.

## <a name="to-use-built-in-colorable-items"></a>Yerleşik renklendirilebilir öğeleri kullanmak için

1. Altında **HKEY_LOCAL_MACHINE\VisualStudio\\< X.Y > \Languages\Language Hizmetleri\\< dil adı\>** burada \<X.Y > sürümüdür [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] ve \<Dil adı > adı adlı bir DWORD kayıt defteri girdisinin değeri, dili, oluşturma **RequestStockColors**.

2. Ayarlama **RequestStockColors** için kayıt defteri girdisinin değeri *1*.

    Kayıt defteri girişinin, uygulamanızın Renklendirici oluşturduktan sonra <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer.ColorizeLine%2A> yöntemi üyelerinin kullanabilir <xref:Microsoft.VisualStudio.TextManager.Interop.DEFAULTITEMS> renk öznitelikleri ' Düzenleyicisi tarafından kullanılmak üzere bir dizi doldurmak için sabit listesi.

   > [!NOTE]
   >  Özel renklendirilebilir öğeler sağlıyorsanız bu kayıt defteri girdisi ayarlamayın. Daha fazla bilgi için [özel renklendirilebilir öğeler](../../extensibility/internals/custom-colorable-items.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Özel düzenleyicilerde söz dizimi renklendirmesi](../../extensibility/syntax-coloring-in-custom-editors.md)
- [Eski dil hizmetinde söz dizimi renklendirmesi](../../extensibility/internals/syntax-coloring-in-a-legacy-language-service.md)
- [Söz dizimi renklendirmesi uygulama](../../extensibility/internals/implementing-syntax-coloring.md)
- [Özel renklendirilebilir öğeler](../../extensibility/internals/custom-colorable-items.md)
- [Eski dil hizmeti kaydedin](../../extensibility/internals/registering-a-legacy-language-service2.md)