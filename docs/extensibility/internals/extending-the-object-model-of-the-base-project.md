---
title: Temel projenin nesne modelini genişletme | Microsoft Docs
ms.date: 03/22/2018
ms.topic: conceptual
helpviewer_keywords:
- automation object model, extending
- project subtypes, extending automation object model
- automation object model
ms.assetid: 2f95cc53-dff6-476c-bacd-500fb0ff7725
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 607a63dc84db2811a4a2d158be07f158b849e1ad
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66329039"
---
# <a name="extend-the-object-model-of-the-base-project"></a>Temel projenin nesne modelini genişletme

Proje alt aşağıdaki yerlerde temel proje Otomasyon nesne modeli genişletebilir:

- Project.Extender("\<ProjectSubtypeName>"): Bir nesne ile özel yöntemleri sunmak bir proje alt böylece <xref:EnvDTE.Project> nesne. Proje alt Otomasyon Genişleticileri kullanıma sunmak için kullanabileceğiniz `Project` nesne. <xref:EnvDTE80.IInternalExtenderProvider> Ana proje alt Toplayıcı üzerinde uygulanan arabirimi, nesne için teklif `VSHPROPID_ExtObjectCATID` gelen <xref:Microsoft.VisualStudio.Shell.Interop.__VSSPROPID2> (karşılık gelen bir `itemid` değerini [VSITEMID. Kök](<xref:Microsoft.VisualStudio.VSConstants.VSITEMID.Root>)) catID.

- ProjectItem.Extender("\<ProjectSubtypeName>"): Böylece, nesnenin belirli özel yöntemlerle sunmak bir proje alt <xref:EnvDTE.ProjectItem> proje içindeki nesne. Proje alt Otomasyon Genişleticileri bu nesneyi göstermek için kullanabilirsiniz. <xref:EnvDTE80.IInternalExtenderProvider> Nesne için teklif gerekiyor ana proje alt Toplayıcı üzerinde uygulanan arabirimi `VSHPROPID_ExtObjectCATID` gelen <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID2> (istenen bir karşılık gelen <xref:Microsoft.VisualStudio.VSConstants.VSITEMID>) catID.

- Project.Properties: Bu koleksiyon bağımsız yapılandırma özelliklerini sunan `Project` nesne. Daha fazla bilgi için `Project` özellikleri görmek <xref:EnvDTE.Project.Properties%2A>. Proje alt Otomasyon Genişleticileri özelliklerini bu koleksiyona eklemek için kullanabilirsiniz. <xref:EnvDTE80.IInternalExtenderProvider> Nesne için teklif gerekiyor ana proje alt Toplayıcı üzerinde uygulanan arabirimi `VSHPROPID_BrowseObjectCATID` gelen <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID2> (karşılık gelen bir `itemid` değerini [VSITEMID. Kök](<xref:Microsoft.VisualStudio.VSConstants.VSITEMID.Root>)) catID.

- Configuration.Properties: Bu koleksiyon (örneğin, hata ayıklama) belirli bir yapılandırma için proje yapılandırması bağımlı özelliklerini sunar. Daha fazla bilgi için bkz. <xref:EnvDTE.Configuration>. Proje alt Otomasyon Genişleticileri özelliklerini bu koleksiyona eklemek için kullanabilirsiniz. <xref:EnvDTE80.IInternalExtenderProvider> Ana proje alt Toplayıcı üzerinde uygulanan arabirimi sunar, nesne için catID `VSHPROPID_CfgBrowseObjectCATID` (karşılık gelen bir `itemid` değerini [VSITEMID. Kök](<xref:Microsoft.VisualStudio.VSConstants.VSITEMID.Root>)). <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgBrowseObject> Arabirimi, bir yapılandırma Gözat nesnesi diğerinden ayırt etmek için kullanılır.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID>