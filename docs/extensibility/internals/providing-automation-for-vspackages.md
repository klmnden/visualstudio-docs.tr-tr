---
title: Vspackage'lar için Otomasyon sağlama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSPackages, automation [Visual Studio SDK]
- automation [Visual Studio SDK], VSPackages
ms.assetid: 104c4c55-78b8-42f4-b6b0-9a334101aaea
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1b72e1493e8ab00f3aa98f3a9bd8e1e1dd30201e
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56614343"
---
# <a name="providing-automation-for-vspackages"></a>VSPackage’lar için Otomasyon Sağlama
Vspackage'lar için Otomasyon sağlamak için iki ana yolu vardır: VSPackage özgü nesneler uygulayarak ve standart Otomasyon nesneleri uygulayarak. Genel olarak, bunlar birlikte otomasyon modeli ortamın genişletmek için kullanılır.

## <a name="vspackage-specific-objects"></a>VSPackage özgü nesneler
 Otomasyon modelindeki belirli yerlerde, VSPackage için benzersiz Otomasyon nesneleri sağlar gerektirir. Örneğin, yeni projeler, VSPackage sağlayan ayrı nesneleri gerektirir. Bu nesnelerin adlarını kayıt defterinde girilen ve ortama yapılan çağrılar aracılığıyla elde edilen `DTE` nesne.

 Standart bir nesne nesne özelliği üzerinden sağlanan nesne bir Otomasyon tüketici kullandığında VSPackage özgü nesneler de elde edilebilir. Örneğin, standart `Window` nesnesinin bir `Object` özelliği, yaygın olarak bilinen `Windows.Object` özelliği. Tüketiciler çağırdığınızda `Window.Object` , VSPackage içinde uygulanan penceresinde geri kendi tasarım belirli bir Otomasyon nesnesinin geçirdiğiniz.

#### <a name="projects"></a>Projeler
 VSPackage kendi VSPackage özgü nesneler aracılığıyla yeni proje türleri için otomasyon modeli genişletebilirsiniz. Nesnenin, VSPackage'ı projenize benzersiz ayırt etmek için yeni Otomasyon nesneleri sağlama birincil amacı bir <xref:Microsoft.VisualStudio.VCProjectEngine.VCProject> veya <xref:VSLangProj80.VSProject2> nesne. Bu ayrım göründükleri yan yana tek veya diğer proje türleri dışında proje türünüzü yinelemek için bir yol sağlamak istediğinizde kullanışlıdır bir çözümde. Daha fazla bilgi için [proje nesnelerini kullanıma sunma](../../extensibility/internals/exposing-project-objects.md).

#### <a name="events"></a>Olaylar
 Olay denetimli mimari ortamın kendi VSPackage özgü nesneler eklemek başka bir yer sağlar. Örneğin, kendi benzersiz olay nesneleri oluşturarak, ortamın olay modeli projeleri için genişletebilirsiniz. Kendi proje türü için yeni bir öğe eklendiğinde kendi olaylarınızı sağlamak isteyebilirsiniz. Daha fazla bilgi için [gösterme olayları](../../extensibility/internals/exposing-events-in-the-visual-studio-sdk.md).

#### <a name="window-objects"></a>Pencere Nesneleri
 Windows, çağrıldığında geri ortama geri VSPackage özgü Otomasyon nesnesi geçirebilirsiniz. Türetilen bir nesne uygulamak <xref:Microsoft.VisualStudio.Shell.Interop.IVsExtensibleObject>, <xref:EnvDTE.IExtensibleObject> veya `IDispatch` , uygulamalı geri özellikleri, onu tarihli pencere nesnesi genişletme. Örneğin, bir pencere çerçevesinde tarihli bir denetim için Otomasyon sağlamak için bu yaklaşımı kullanabilirsiniz. Bu nesne ve genişletme herhangi bir nesne semantiği tasarlamak için size aittir. Daha fazla bilgi için [nasıl yapılır: Windows için Otomasyon sağlar](../../extensibility/internals/how-to-provide-automation-for-windows.md).

#### <a name="options-pages-on-the-tools-menu"></a>Araçlar menüsünde Seçenekler sayfaları
 Araçlar, Seçenekler otomasyon modeli sayfaları uygulama ve kendi seçenekleri oluşturmak üzere kayıt defteri bilgileri ekleyerek aracılığıyla genişletmek için sayfaları oluşturabilirsiniz. Diğer Seçenekler sayfaları gibi ortam nesne modeli üzerinden sayfalarınızı ardından volat pouze jednou. Tasarım ortamı üzerinden VSPackages ekleme özelliği seçenekler sayfaları gerektiriyorsa, Otomasyon desteği de eklemeniz gerekir. Daha fazla bilgi için [seçenekler sayfaları için Otomasyon desteği](../../extensibility/internals/automation-support-for-options-pages.md).

## <a name="standard-automation-objects"></a>Standart Otomasyon nesneleri
 Otomasyon projeleri için genişletmek için de standart Otomasyon nesneleri uygular (türetilen `IDispatch`) diğer proje nesneler dikkati ve standart yöntemleri ve özellikleri uygulama. Örnekler, standart nesneleri gibi çözüm hiyerarşiye eklenen proje nesnelerini `Projects`, `Project`, `ProjectItem`, ve `ProjectItems`. Her yeni proje türü, bu nesneler (ve muhtemelen diğer formüllerde semantiği bağlı olarak, projenizin) uygulamanız gerekir.

 Bir anlamda, bu nesneler VSPackage özgü proje nesnelerini karşı avantajı sağlar. Projeniz gibi aynı nesneleri destekleyen başka bir projeye genelleştirilmiş bir yol kullanılması standart Otomasyon nesneleri sağlar. Bu nedenle, bir genel karşı yazılan eklenti `Project` ve `ProjectItem` nesneleri herhangi bir türde projelere karşı işlev görebilir. Daha fazla bilgi için [modelleme projesi](../../extensibility/internals/project-modeling.md).