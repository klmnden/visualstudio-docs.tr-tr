---
title: Proje bağlamı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio SDK], opening items
ms.assetid: d1803f4a-24eb-44b0-b5d2-cb40c15534be
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: cd9d4c93ac69c73f81adc3111b0aeb4e141ab39f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54990335"
---
# <a name="project-context"></a>Proje Bağlamı
Kullanıcı ekler veya projeleri ve proje öğeleri ile birlikte çalışır, IDE proje bağlam kavramı nasıl çeşitli işlemler gerçekleştirilmelidir belirlemek için kullanır.  
  
 Genellikle, dosyaları seçerek kullanıcı açıkça oluşturan standart proje nesnelerdir **yeni proje** komut veya seçerek kullanılabilir yapar **Proje Aç** komutunu  **Dosya** menüsü. Bu gibi durumlarda, dosyalar oluşturulur ve bir proje bağlamında açılır ve proje türü belge düzenleme bağlamı tanımlar.  
  
 Bazı projeler çok zengin bir bağlam sağlar. Örneğin, bir proje kapsamlı, programlı bir ad alanı veya proje kapsamlı veritabanı bağlantısı veri bağlama için proje yönetir. Kullanıcının sık dosyaları veya veritabanı bağlantıları görüntülenen Çözüm Gezgini'nde bir proje öğesi gibi bir özel Proje nesne kullanarak doğrudan açabilirsiniz.  
  
 Diğer zamanlarda ise, öğenin proje bağlamı açıkça belirtilmedi. Kullanıcı seçerek bir dosya açıldığında, örneğin, bir öğenin bağlam kullanılamıyor **mevcut Dosya Aç** komutunu **dosya** hata ayıklayıcıyı bir dosya veya kullanıcı tıkladığında çalıştığında menüsü **Dosyalarda Bul** komutunu **Bul ve Değiştir** iletişim kutusu. Bu durumlarda, IDE aramaları işlenecek <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument> bir belgeyi açmak için en iyi proje bulma işlemini yönetmek için.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Proje önceliği](../../extensibility/internals/project-priority.md)   
 [Proje ve Proje Öğesi Şablonları Ekleme](../../extensibility/internals/adding-project-and-project-item-templates.md)