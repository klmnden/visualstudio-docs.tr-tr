---
title: Seçenekler sayfaları için Otomasyon desteği | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Tools Options pages [Visual Studio SDK], automation support
- automation [Visual Studio SDK], creating Tools Options pages
ms.assetid: 0b25b82c-7432-4e0a-9e84-350269ba8260
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0bf997205979cdfbb9c9f03492a5943f458e2d9c
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66342268"
---
# <a name="automation-support-for-options-pages"></a>Seçenekler sayfaları için Otomasyon desteği
VSPackage özel sağlayabilir **seçenekleri** iletişim kutuları için **Araçları** menü (**Araçlar Seçenekler** sayfaları) içinde [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] ve bunları Otomasyon için kullanılabilir hale getirebilirsiniz Model.

## <a name="tools-options-pages"></a>Araçlar Seçenekler sayfaları
 Oluşturmak için bir **Araçlar Seçenekler** sayfasında VSPackage VSPackage'nın uygulaması aracılığıyla ortamına döndürülen bir kullanıcı denetimi uygulama sağlamalıdır <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetPropertyPage%2A> yöntemi. (Veya yönetilen kod, <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetPropertyPage%2A> yöntemi.)

 Bu isteğe bağlıdır, ancak bu yeni sayfa otomasyon modeli aracılığıyla erişmesine izin vermek için önemle önerilir. Aşağıdaki adımlarla bunu yapabilirsiniz:

1. Genişletme <xref:EnvDTE._DTE.Properties%2A> IDispatch türetilmiş bir nesnenin uygulanmasına aracılığıyla nesne.

2. Uygulanışı dönüş <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetAutomationObject%2A> yöntemi (veya yönetilen kod için <xref:Microsoft.VisualStudio.Shell.Package.GetAutomationObject%2A> yöntemi) IDispatch türetilmiş nesne.

3. Bir Otomasyon tüketici çağırdığında <xref:EnvDTE._DTE.Properties%2A> özel metodunda **seçeneği** özellik sayfası, ortam kullanır <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetAutomationObject%2A> özel elde etmek için yöntemi **Araçlar Seçenekler** sayfanın Otomasyon uygulama.

4. Otomasyon nesne VSPackage'ı, ardından her sağlamak için kullanılan <xref:EnvDTE.Property> tarafından döndürülen <xref:EnvDTE._DTE.Properties%2A>.

   Özel bir uygulama örneği **Araçlar Seçenekler** sayfasında, bkz: [VSSDK örnekleri](https://aka.ms/vs2015sdksamples).

## <a name="see-also"></a>Ayrıca bkz.
- [Proje nesnelerini kullanıma sunma](../../extensibility/internals/exposing-project-objects.md)