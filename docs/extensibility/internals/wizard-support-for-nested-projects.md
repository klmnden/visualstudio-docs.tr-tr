---
title: İç içe projeler için sihirbaz desteği | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Add Item wizard
- nested projects, wizard support
- New Project wizard
ms.assetid: 1b496acc-b326-4cdb-bb48-e3b5c6f12e05
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2635488c970e0f2b134bf4d54fa6a364a5b30198
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55004766"
---
# <a name="wizard-support-for-nested-projects"></a>İç içe Projeler için Sihirbaz Desteği
IDE ana proje iç içe projeler için uygulayabileceğiniz iki sihirbazları çalıştırır: **yeni proje** Sihirbazı ve **Öğe Ekle** Sihirbazı.  
  
 Bir kullanıcı başlarsa **yeni proje** seçerek Sihirbazı **Proje Ekle** tıklayıp **yeni proje** Dosya menüsünden veya seçerek **Ekle** sağ **yeni proje** IDE Çözüm Gezgini'nde çalışan **AddProject** komut ve üst projenin uygulaması **AddProject**komut ya da bir şablon proje dosyası veya bir dizi bağlam parametreleri içeren bir sihirbaz (.vsz) dosyası döndürür.  
  
 Benzer şekilde, bir üst projenin uygulaması **addItem** sihirbazları farklı bir bağlam parametreleri kümesini içeren bir .vsz dosyası döndürür.  
  
 Sihirbazları hakkında daha fazla bilgi için bkz: [Sihirbazı (. Vsz) dosya](../../extensibility/internals/wizard-dot-vsz-file.md), [bağlam parametreleri](../../extensibility/internals/context-parameters.md) ve [proje ve öğe şablonlarını kaydetme](../../extensibility/internals/registering-project-and-item-templates.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy>   
 [Projeleri İç İçe Geçirme](../../extensibility/internals/nesting-projects.md)