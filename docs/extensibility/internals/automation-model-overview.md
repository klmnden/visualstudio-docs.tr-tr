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
ms.openlocfilehash: 4f13ffca7dc39be65f8a36a9b242bf7f0f82dc4c
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60061534"
---
# <a name="automation-model-overview"></a>Otomasyon modeline genel bakış
Otomasyon modeli karşı bir Visual Studio eklentisi veya uzantı yazabilirsiniz nesnelerin bir kümesinden oluşur. Bir eklenti, Visual Studio ortamını yönetmek ve ortak görevleri otomatikleştirme bir uygulamadır. Visual Studio uzantısı özel Visual Studio bileşenlerini oluşturabilir veya metin düzenleyicisi gibi standart bileşenlerin işlevselliğini ekleyin.

## <a name="objects-in-the-automation-model"></a>Otomasyon modelindeki nesneler
 Otomasyon modeli, ortak bir ortam, ana özelliklerini denetleyen nesnelerin ilgili grubundan oluşur. Aşağıdaki diyagramda, kapsamlı otomasyon modeli oluşturan Visual Studio nesne kümesini gösterir.

 ![Visual Studio Otomasyon nesnesi grafiği](../../extensibility/internals/media/vsvisualstudioautomationobjectchart.gif "vsVisualStudioAutomationObjectChart")

 Daha fazla bilgi için [Visual Studio ortamını genişletme](https://msdn.microsoft.com/Library/4173a963-7ac7-4966-9bb7-e28a9d9f6792).

 Ortamı farklı işlevsel alanları için bir model sağlar. Örneğin, kod içinde bulabileceğiniz çeşitli öğeleri için bir kod modeli yoktur. Çeşitli belge öğeleri için bir belge modeli yoktur. VSPackage sağlayıcıları özellikle ilgisini çeken bir alan, Proje alanı var. Büyük olasılıkla çok aynı şekilde Otomasyon modeline katkıda bulunmak için yeni proje türleri isteyeceksiniz [!INCLUDE[vcprvc](../../code-quality/includes/vcprvc_md.md)] ve [!INCLUDE[vbprvb](../../code-quality/includes/vbprvb_md.md)] Otomasyon modeline katkıda bulunun. İşlem açıklandığı [Vspackage'lar için Otomasyon sağlar](../../extensibility/internals/providing-automation-for-vspackages.md).

 Yerleri burada ortamın Otomasyon modelini genişletme düşünebilirsiniz:

- Project

- Belge

- Kod

- Yapı

Otomasyon ile ilgili daha fazla bilgi için bkz [Visual Studio için otomasyon ve genişletilebilirlik](../extensibility-in-visual-studio.md). Bu belge ve belgeler, otomasyon, VSPackage için nasıl sağladığını ile ilgili kararlar almanıza yardımcı olmak için bağlantılar sağlar.

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Bir eklenti oluşturun](https://msdn.microsoft.com/Library/50be56d2-e3a5-4cd2-8569-2a0666b268ce)