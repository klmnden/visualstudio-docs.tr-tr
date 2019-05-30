---
title: Proje bağlamı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio SDK], opening items
ms.assetid: d1803f4a-24eb-44b0-b5d2-cb40c15534be
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 175ee37628b1794377a6b4e9e94cef52466cd291
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66328353"
---
# <a name="project-context"></a>Proje Bağlamı
Kullanıcı ekler veya projeleri ve proje öğeleri ile birlikte çalışır, IDE proje bağlam kavramı nasıl çeşitli işlemler gerçekleştirilmelidir belirlemek için kullanır.

 Genellikle, dosyaları seçerek kullanıcı açıkça oluşturan standart proje nesnelerdir **yeni proje** komut veya seçerek kullanılabilir yapar **Proje Aç** komutunu  **Dosya** menüsü. Bu gibi durumlarda, dosyalar oluşturulur ve bir proje bağlamında açılır ve proje türü belge düzenleme bağlamı tanımlar.

 Bazı projeler çok zengin bir bağlam sağlar. Örneğin, bir proje kapsamlı, programlı bir ad alanı veya proje kapsamlı veritabanı bağlantısı veri bağlama için proje yönetir. Kullanıcının sık dosyaları veya veritabanı bağlantıları görüntülenen Çözüm Gezgini'nde bir proje öğesi gibi bir özel Proje nesne kullanarak doğrudan açabilirsiniz.

 Diğer zamanlarda ise, öğenin proje bağlamı açıkça belirtilmedi. Kullanıcı seçerek bir dosya açıldığında, örneğin, bir öğenin bağlam kullanılamıyor **mevcut Dosya Aç** komutunu **dosya** hata ayıklayıcıyı bir dosya veya kullanıcı tıkladığında çalıştığında menüsü **Dosyalarda Bul** komutunu **Bul ve Değiştir** iletişim kutusu. Bu durumlarda, IDE aramaları işlenecek <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument> bir belgeyi açmak için en iyi proje bulma işlemini yönetmek için.

## <a name="see-also"></a>Ayrıca Bkz.
- [Proje Önceliği](../../extensibility/internals/project-priority.md)
- [Proje ve Proje Öğesi Şablonları Ekleme](../../extensibility/internals/adding-project-and-project-item-templates.md)