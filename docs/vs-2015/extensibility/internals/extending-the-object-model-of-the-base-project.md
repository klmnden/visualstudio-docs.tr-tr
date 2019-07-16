---
title: Temel projenin nesne modelini genişletme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- automation object model, extending
- project subtypes, extending automation object model
- automation object model
ms.assetid: 2f95cc53-dff6-476c-bacd-500fb0ff7725
caps.latest.revision: 18
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 7723881bce81824b66a936793175077a0ec67666
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68187162"
---
# <a name="extending-the-object-model-of-the-base-project"></a>Temel Projenin Nesne Modelini Genişletme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Proje alt aşağıdaki yerlerde temel proje Otomasyon nesne modeli genişletebilir:  
  
- Project.Extender ("\<ProjectSubtypeName >") – özel yöntemleri ile bir nesne sunmak bir proje alt böylece <xref:EnvDTE.Project>. Proje alt Otomasyon Genişleticileri kullanıma sunmak için kullanabileceğiniz `Project` nesne. <xref:EnvDTE80.IInternalExtenderProvider>Ana proje alt Toplayıcı üzerinde uygulanan arabirimi, nesne için teklif `VSHPROPID_ExtObjectCATID` gelen <xref:Microsoft.VisualStudio.Shell.Interop.__VSSPROPID2> (karşılık gelen bir `itemid` VSITEMID_ROOT, değerini gelen `VSITEMID`) catID.  
  
- ProjectItem.Extender ("\<ProjectSubtypeName >") – bir nesne, belirli özel yöntemlerle sunmak bir proje alt böylece <xref:EnvDTE.ProjectItem> proje içindeki nesne. Proje alt Otomasyon Genişleticileri bu nesneyi göstermek için kullanabilirsiniz. <xref:EnvDTE80.IInternalExtenderProvider> Nesne için teklif gerekiyor ana proje alt Toplayıcı üzerinde uygulanan arabirimi `VSHPROPID_ExtObjectCATID` gelen <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID2> (istenen bir karşılık gelen `VSITEMID`) catID.  
  
- Project.Properties – Bu koleksiyonu yapılandırma bağımsız özelliklerini sunan `Project` nesne. Proje özellikleri hakkında daha fazla bilgi için bkz. <xref:EnvDTE.Project.Properties%2A>. Proje alt Otomasyon Genişleticileri özelliklerini bu koleksiyona eklemek için kullanabilirsiniz. <xref:EnvDTE80.IInternalExtenderProvider> Nesne için teklif gerekiyor ana proje alt Toplayıcı üzerinde uygulanan arabirimi `VSHPROPID_BrowseObjectCATID` VSHPROPID2 gelen (karşılık gelen bir `itemid` VSITEMID_ROOT, değerini gelen <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID2>) catID.  
  
- Configuration.Properties – Bu koleksiyonun yapılandırma bağımlı özelliklerine (örneğin, hata ayıklama) belirli bir yapılandırma için projeyi kullanıma sunar. Daha fazla bilgi edinmek, <xref:EnvDTE.Configuration>. Proje alt Otomasyon Genişleticileri özelliklerini bu koleksiyona eklemek için kullanabilirsiniz. <xref:EnvDTE80.IInternalExtenderProvider> Ana proje alt Toplayıcı üzerinde uygulanan arabirimi sunar, nesne için catID `VSHPROPID_CfgBrowseObjectCATID` (karşılık gelen bir `itemid` değerini <xref:Microsoft.VisualStudio.VSConstants.VSITEMID>). <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgBrowseObject>Arabirimi, bir yapılandırma Gözat nesnesi diğerinden ayırt etmek için kullanılır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID>
