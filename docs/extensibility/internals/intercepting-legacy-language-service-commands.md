---
title: Eski dil hizmeti komutlarını kesme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- commands, intercepting language service
- language services, intercepting commands
ms.assetid: eea69f03-349c-44bb-bd4f-4925c0dc3e55
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: eb53de9cf4d3056d9a07a915267391de27b753fb
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56614915"
---
# <a name="intercepting-legacy-language-service-commands"></a>Eski Dil Hizmeti Komutlarını Kesme
İle [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)], metin görünümünü aksi işlemek dil hizmeti ıntercept komutları olabilir. Bu metin görünümünü değil yönetmiyor dile özgü davranışı için kullanışlıdır. Bu komutlar, dil hizmetinizden metin görünümü bir veya daha fazla komut filtreler ekleyerek yakalayabilirsiniz.

## <a name="getting-and-routing-the-command"></a>Alma ve komut yönlendirme
 Bir komut filtresi bir <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> belirli karakter dizileri veya anahtar komutları izleyen bir nesne. Tek metin görünümle birden fazla komut filtre ilişkilendirebilirsiniz. Her metin görünümünü bir komuta zincirini filtreleri korur. Yeni bir komut filtre oluşturduktan sonra uygun bir metin görünümünü zincirinde için filtre ekleyin.

 Çağrı <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.AddCommandFilter%2A> metodunda <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView> zinciri, komut filtre eklemek için. Çağırdığınızda <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.AddCommandFilter%2A>, [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] komut filtrenizle işlemiyor komutları geçirmek başka bir komut filtre döndürür.

 Komut işleme için aşağıdaki seçenekleriniz vardır:

- Komutu işlemek ve ardından sonraki komut filtre açın komut zincirinde geçirin.

- Komutu işlemek ve sonraki komutu filtre açın komutu kodum'a geçirmez.

- Komutunu işleyemez, ancak sonraki komut filtre açın komutu geçirin.

- Komut yoksayın. Geçerli filtreye işlemez ve sıradaki filtreye açın geçirmeyin.

  Dil hizmetinizin hangi komutları işlemek için bilgi [dil hizmeti filtreleri için önemli komutlar](../../extensibility/internals/important-commands-for-language-service-filters.md).