---
title: IDE tanımlı komutlar, menüler ve gruplar | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- commands, environment-defined
- .vsct files, environment-defined constants
- command groups, environment-defined
ms.assetid: 86b3af13-7163-48c6-986b-7beeedbc26cc
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: c9735a1ef80c22a9bf81edc711ef0f8819114720
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53941131"
---
# <a name="ide-defined-commands-menus-and-groups"></a>IDE Tanımlı Komutlar, Menüler ve Gruplar
Birçok menüler, komutları ve komut grupları zaten tarafından tanımlanan [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE. Bu komutlar da genişlettiğinizde, kullanımınıza sunulan. [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].  
  
## <a name="finding-environment-defined-commands"></a>Ortam tanımlı komutları bulma  
 Ortam komutları dört .vsct dosyaları kümesi içinde tanımlanır:  
  
- SharedCmdDef.vsct  
  
- SharedCmdPlace.vsct  
  
- ShellCmdDef.vsct  
  
- ShellCmdPlace.vsct  
  
  Bu dosyalar bulunur  *\<Visual Studio SDK'sını yükleme yolu >* \VisualStudioIntegration\Common\Inc\\. Bu dosyalar, menüler ve kendi menüler, gruplar ve komutlar için kapsayıcı olarak, VSPackage'ı komut tablosu (.vsct) yapılandırma dosyasında kullanabileceğiniz grupların GUID'leri ve tanımları sağlar.  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Visual Studio Menülerinin GUID’leri ve Kimlikleri](../../extensibility/internals/guids-and-ids-of-visual-studio-menus.md)  
 Visual Studio menü çubuğundaki menüleri ve içerdikleri tüm grupların GUID ve ID değerleri sağlar.  
  
 [Visual Studio Araç Çubuklarının GUID’leri ve Kimlikleri](../../extensibility/internals/guids-and-ids-of-visual-studio-toolbars.md)  
 Visual Studio IDE'de araç çubukları ve içerdikleri tüm grupların GUID ve ID değerleri sağlar.  
  
 [Visual Studio Komutlarının GUID’leri ve Kimlikleri](../../extensibility/internals/guids-and-ids-of-visual-studio-commands.md)  
 Tarafından Visual Studio IDE tanımlı komutlar GUID ve ID değerini verir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio komut tablosu (. Vsct) dosyaları](../../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)   
 [Proje sistemlerini genişletmeye yönelik IDE tanımlı komutlar](../../extensibility/internals/ide-defined-commands-for-extending-project-systems.md)   
 [VSPackage’ların Kullanıcı Arabirimi Öğeleri Eklemesi](../../extensibility/internals/how-vspackages-add-user-interface-elements.md)