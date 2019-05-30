---
title: Eski dil hizmeti komutlarını kesme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- commands, intercepting language service
- language services, intercepting commands
ms.assetid: eea69f03-349c-44bb-bd4f-4925c0dc3e55
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3716f02b076bd5ea7ef63135133acffc823a7703
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66314938"
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