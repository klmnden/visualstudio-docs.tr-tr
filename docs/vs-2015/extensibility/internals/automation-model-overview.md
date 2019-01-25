---
title: Otomasyon modeline genel bakış | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- automation [Visual Studio SDK], about automation
- extensibility
ms.assetid: 12b6d6db-0d22-4aaa-aa7d-1365f759b7b0
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 0eb1d870b3858255fe6b4a0cf9a255d9d1df8c59
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54770243"
---
# <a name="automation-model-overview"></a>Otomasyon Modeline Genel Bakış
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Otomasyon modeli karşı bir Visual Studio eklentisi veya uzantı yazabilirsiniz nesnelerin bir kümesinden oluşur. Bir eklenti, Visual Studio ortamını yönetmek ve ortak görevleri otomatikleştirme bir uygulamadır. Visual Studio uzantısı özel Visual Studio bileşenlerini oluşturabilir veya metin düzenleyicisi gibi standart bileşenlerin işlevselliğini ekleyin.  
  
## <a name="objects-in-the-automation-model"></a>Otomasyon modelindeki nesneler  
 Otomasyon modeli, ortak bir ortam, ana özelliklerini denetleyen nesnelerin ilgili grubundan oluşur. Otomasyon modeli oluşturan nesne kapsamlı kümesini gösteren bir diyagram verilmiştir.  
  
 ![Visual Studio Otomasyon nesnesi grafiği](../../extensibility/internals/media/vsvisualstudioautomationobjectchart.gif "vsVisualStudioAutomationObjectChart")  
Visual Studio Otomasyon nesneleri  
  
 Daha fazla bilgi için [Visual Studio ortamını genişletme](http://msdn.microsoft.com/library/4173a963-7ac7-4966-9bb7-e28a9d9f6792).  
  
 Ortamı farklı işlevsel alanları için bir model sağlar. Örneğin, kod içinde bulabileceğiniz çeşitli öğeleri için bir kod modeli yoktur. Çeşitli belge öğeleri için bir belge modeli yoktur. VSPackage sağlayıcıları özellikle ilgisini çeken bir alan, Proje alanı var. Büyük olasılıkla çok aynı şekilde Otomasyon modeline katkıda bulunmak için yeni proje türleri isteyeceksiniz [!INCLUDE[vcprvc](../../includes/vcprvc-md.md)] ve [!INCLUDE[vbprvb](../../includes/vbprvb-md.md)] Otomasyon modeline katkıda bulunun. İşlem açıklandığı [Vspackage'lar için Otomasyon sağlama](../../extensibility/internals/providing-automation-for-vspackages.md).  
  
 Yerleri burada ortamın Otomasyon modelini genişletme düşünebilirsiniz:  
  
- Proje  
  
- Belge  
  
- Kod  
  
- Derleme  
  
  Otomasyon ile ilgili daha fazla bilgi için bkz [Visual Studio için otomasyon ve genişletilebilirlik](http://msdn.microsoft.com/library/f71a2253-3e68-4e5e-9a18-edbba816caf6). Bu belge ve belgeler, otomasyon, VSPackage için nasıl sağladığını ile ilgili kararlar almanıza yardımcı olmak için bağlantılar sağlar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Bir eklenti oluşturma](http://msdn.microsoft.com/library/50be56d2-e3a5-4cd2-8569-2a0666b268ce)
