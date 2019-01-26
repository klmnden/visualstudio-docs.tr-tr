---
title: Otomasyon modeline genel bakış | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- automation [Visual Studio SDK], about automation
- extensibility
ms.assetid: 12b6d6db-0d22-4aaa-aa7d-1365f759b7b0
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 65698c140647831ab329069e61e2cc5ea826d6e5
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54992119"
---
# <a name="automation-model-overview"></a>Otomasyon modeline genel bakış
Otomasyon modeli karşı bir Visual Studio eklentisi veya uzantı yazabilirsiniz nesnelerin bir kümesinden oluşur. Bir eklenti, Visual Studio ortamını yönetmek ve ortak görevleri otomatikleştirme bir uygulamadır. Visual Studio uzantısı özel Visual Studio bileşenlerini oluşturabilir veya metin düzenleyicisi gibi standart bileşenlerin işlevselliğini ekleyin.  
  
## <a name="objects-in-the-automation-model"></a>Otomasyon modelindeki nesneler  
 Otomasyon modeli, ortak bir ortam, ana özelliklerini denetleyen nesnelerin ilgili grubundan oluşur. Aşağıdaki diyagramda, kapsamlı otomasyon modeli oluşturan Visual Studio nesne kümesini gösterir.  
  
 ![Visual Studio Otomasyon nesnesi grafiği](../../extensibility/internals/media/vsvisualstudioautomationobjectchart.gif "vsVisualStudioAutomationObjectChart")  
  
 Daha fazla bilgi için [Visual Studio ortamını genişletme](https://msdn.microsoft.com/Library/4173a963-7ac7-4966-9bb7-e28a9d9f6792).  
  
 Ortamı farklı işlevsel alanları için bir model sağlar. Örneğin, kod içinde bulabileceğiniz çeşitli öğeleri için bir kod modeli yoktur. Çeşitli belge öğeleri için bir belge modeli yoktur. VSPackage sağlayıcıları özellikle ilgisini çeken bir alan, Proje alanı var. Büyük olasılıkla çok aynı şekilde Otomasyon modeline katkıda bulunmak için yeni proje türleri isteyeceksiniz [!INCLUDE[vcprvc](../../code-quality/includes/vcprvc_md.md)] ve [!INCLUDE[vbprvb](../../code-quality/includes/vbprvb_md.md)] Otomasyon modeline katkıda bulunun. İşlem açıklandığı [Vspackage'lar için Otomasyon sağlar](../../extensibility/internals/providing-automation-for-vspackages.md).  
  
 Yerleri burada ortamın Otomasyon modelini genişletme düşünebilirsiniz:  
  
-   Proje  
  
-   Belge  
  
-   Kod  
  
-   Derleme  

  
Otomasyon ile ilgili daha fazla bilgi için bkz [Visual Studio için otomasyon ve genişletilebilirlik](../extensibility-in-visual-studio.md). Bu belge ve belgeler, otomasyon, VSPackage için nasıl sağladığını ile ilgili kararlar almanıza yardımcı olmak için bağlantılar sağlar.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Bir eklenti oluşturun](https://msdn.microsoft.com/Library/50be56d2-e3a5-4cd2-8569-2a0666b268ce)