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
ms.openlocfilehash: e17164976062ec916074c6210be6ae42e8ea1d03
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65699496"
---
# <a name="automation-model-overview"></a>Otomasyon Modeline Genel Bakış
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Otomasyon modeli karşı bir Visual Studio eklentisi veya uzantı yazabilirsiniz nesnelerin bir kümesinden oluşur. Bir eklenti, Visual Studio ortamını yönetmek ve ortak görevleri otomatikleştirme bir uygulamadır. Visual Studio uzantısı özel Visual Studio bileşenlerini oluşturabilir veya metin düzenleyicisi gibi standart bileşenlerin işlevselliğini ekleyin.  
  
## <a name="objects-in-the-automation-model"></a>Otomasyon modelindeki nesneler  
 Otomasyon modeli, ortak bir ortam, ana özelliklerini denetleyen nesnelerin ilgili grubundan oluşur. Otomasyon modeli oluşturan nesne kapsamlı kümesini gösteren bir diyagram verilmiştir.  
  
 ![Visual Studio Otomasyon nesnesi grafiği](../../extensibility/internals/media/vsvisualstudioautomationobjectchart.gif "vsVisualStudioAutomationObjectChart")  
Visual Studio Otomasyon nesneleri  
  
 Daha fazla bilgi için [Visual Studio ortamını genişletme](https://msdn.microsoft.com/library/4173a963-7ac7-4966-9bb7-e28a9d9f6792).  
  
 Ortamı farklı işlevsel alanları için bir model sağlar. Örneğin, kod içinde bulabileceğiniz çeşitli öğeleri için bir kod modeli yoktur. Çeşitli belge öğeleri için bir belge modeli yoktur. VSPackage sağlayıcıları özellikle ilgisini çeken bir alan, Proje alanı var. Büyük olasılıkla çok aynı şekilde Otomasyon modeline katkıda bulunmak için yeni proje türleri isteyeceksiniz [!INCLUDE[vcprvc](../../includes/vcprvc-md.md)] ve [!INCLUDE[vbprvb](../../includes/vbprvb-md.md)] Otomasyon modeline katkıda bulunun. İşlem açıklandığı [Vspackage'lar için Otomasyon sağlama](../../extensibility/internals/providing-automation-for-vspackages.md).  
  
 Yerleri burada ortamın Otomasyon modelini genişletme düşünebilirsiniz:  
  
- Project  
  
- Belge  
  
- Kod  
  
- Yapı  
  
  Otomasyon ile ilgili daha fazla bilgi için bkz [Visual Studio için otomasyon ve genişletilebilirlik](https://msdn.microsoft.com/library/f71a2253-3e68-4e5e-9a18-edbba816caf6). Bu belge ve belgeler, otomasyon, VSPackage için nasıl sağladığını ile ilgili kararlar almanıza yardımcı olmak için bağlantılar sağlar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Bir eklenti oluşturma](https://msdn.microsoft.com/library/50be56d2-e3a5-4cd2-8569-2a0666b268ce)
