---
title: Düzenleyici ve dil hizmeti uzantıları | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- editors [Visual Studio SDK]
ms.assetid: 5653bac9-724f-4948-a820-68ce6aa96365
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 5512aa9fc40e9f2ef7619cc5cf80f2751de15327
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49265985"
---
# <a name="editor-and-language-service-extensions"></a>Düzenleyici ve Dil Hizmeti Uzantıları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Çoğu Visual Studio Kod Düzenleyicisi özelliklerini genişletebilirsiniz. Düzenleyici, Windows Presentation Foundation (WPF) dayanır ve yönetilen kodda yazılır. Bu tasarım, Visual Studio'nun önceki sürümlerinde tasarımları farklıdır, aynı özelliklerin çoğunu sağlar. Düzenleyiciyi genişletmek için Yönetilen Genişletilebilirlik Çerçevesi (MEF) kullanın.  
  
 Visual Studio SDK'sı olarak da bilinen bağdaştırıcıları sağlar *dolgular* önceki sürümleri için yazılmış VSPackages desteklemek için. Bununla birlikte, mevcut bir VSPackage varsa, daha iyi performans ve güvenilirlik elde etmek için yeni teknoloji güncelleştirme öneririz.  
  
## <a name="related-topics"></a>İlgili Konular  
  
|Başlık|Açıklama|  
|-----------|-----------------|  
|[Düzenleyici Öğesi Şablonuyla Uzantı Oluşturma](../extensibility/creating-an-extension-with-an-editor-item-template.md)|Düzenleyici öğesi şablonlarını kullanarak giriş.|  
|[Düzenleyiciyi ve Dil Hizmetlerini Genişletme](../extensibility/extending-the-editor-and-language-services.md)|Tasarım ve çekirdek Düzenleyici özelliklerini tanıtır ve genişletmek nasıl Göster belgelere bağlantılar.|  
|[Düzenleyicideki Eski Arabirimler](../extensibility/legacy-interfaces-in-the-editor.md)|Mevcut koddan çekirdek Düzenleyicisi'ne erişmek nasıl açıklayan belgelere bağlantılar.|  
|[Özel Düzenleyiciler ve Tasarımcılar Oluşturma](../extensibility/creating-custom-editors-and-designers.md)|Özel düzenleyicilerde nasıl oluşturulacağını açıklayan belgelere bağlantılar.|  
|[Eski Dil Hizmeti Genişletilebilirliği](../extensibility/internals/legacy-language-service-extensibility.md)|Programlama dilleri Visual Studio ile tümleştirmek nasıl açıklayan belgelere bağlantılar.|  
|[Managed Extensibility Framework (MEF)](http://msdn.microsoft.com/library/6c61b4ec-c6df-4651-80f1-4854f8b14dde)|Yönetilen Genişletilebilirlik Çerçevesi (MEF) sunar.|  
|[Windows Presentation Foundation](http://msdn.microsoft.com/library/f667bd15-2134-41e9-b4af-5ced6fafab5d)|Windows Presentation Foundation (WPF) sunar.|

