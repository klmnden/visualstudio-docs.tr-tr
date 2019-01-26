---
title: Projeleri ve dosyaları için şablonlar
ms.date: 01/02/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- templates [Visual Studio], project
- templates [Visual Studio], item
- item templates [Visual Studio]
- project templates [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: f4c63ab9cfe055d5e1b5a9deeae29ed49b277e9a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55006818"
---
# <a name="project-and-item-templates"></a>Proje ve öğe şablonları

Proje ve öğe şablonları, bazı temel kod ve kendi amaçları için özelleştirebilecekleri yapısı, kullanıcılara vermek yeniden kullanılabilir saptamalar sağlar.

## <a name="visual-studio-templates"></a>Visual Studio şablonları

Bir dizi önceden tanımlanmış proje ve öğe şablonları, Visual Studio ile yüklenir. Örneğin, Visual Basic ve C# **Windows Forms uygulaması** ve **sınıf kitaplığı** gösterilir şablonları **yeni proje** iletişim kutusu olan proje şablonları. Öğe şablonları göster **Yeni Öğe Ekle** iletişim kutusu ve kod dosyaları, XML dosyaları, HTML sayfaları ve stil sayfalarını gibi öğeleri içerir.

Bu şablonlar, proje oluşturmaya başlamak için veya mevcut projeleri genişletmek için kullanıcılar için bir başlangıç noktası sağlar. Proje şablonları, belirli proje türü için gerekli dosyaları sağlar, standart derleme başvurularını içerir ve varsayılan proje özellikleri ve derleyici seçeneklerini ayarlayın. Öğe şablonları, birden çok kaynak kodu dosyaları saplama kodla, Tasarımcı bilgi dosyaları ve gömülü kaynaklar belirli dosya uzantısına sahip tek bir boş dosya karmaşıklığı değişebilir.

Yüklü şablon olarak kullanabileceğiniz **yeni proje** ve **Yeni Öğe Ekle** iletişim kutuları, kendi şablonlarınızı yazar veya indirin ve topluluk tarafından oluşturulan şablonlarını kullanın. Daha fazla bilgi için [nasıl yapılır: Proje şablonları oluşturma](../ide/how-to-create-project-templates.md) ve [nasıl yapılır: Öğe şablonları oluşturma](../ide/how-to-create-item-templates.md).

## <a name="contents-of-a-template"></a>Bir şablon içeriği

Tüm proje ve öğe şablonları, Visual Studio ile yüklenir veya sizin tarafınızdan oluşturulan aynı ilkeleri kullanarak işlev ve benzer içeriğe sahip. Tüm şablonları aşağıdaki öğeleri içerir:

- Şablonu kullanıldığında oluşturulan dosyalar. Bu dosyalar, kaynak kodu dosyaları, katıştırılmış kaynaklar, proje dosyaları vb. içerir.

- Bir *.vstemplate* şablonda görüntülemek için gerekli meta veriler içeren dosya **yeni proje** ve **Yeni Öğe Ekle** iletişim kutuları ve bir proje oluşturun veya öğesini şablonu. Hakkında daha fazla bilgi için *.vstemplate* dosyaları görmek [şablon parametreleri](../ide/template-parameters.md).

Ne zaman bu dosyaları sıkıştırılır içine bir *.zip* dosya ve doğru klasöre yerleştirin, Visual Studio otomatik olarak aşağıdaki konumlarda görüntüler:

- Proje şablonları görünür **yeni proje** iletişim kutusu.

- Öğe şablonları görünür **Yeni Öğe Ekle** iletişim kutusu.

Şablon klasörleri hakkında daha fazla bilgi için bkz. [nasıl yapılır: Şablonları bulma ve düzenleme](../ide/how-to-locate-and-organize-project-and-item-templates.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Proje şablonları oluşturma](../ide/how-to-create-project-templates.md)
- [Nasıl yapılır: Öğe şablonları oluşturma](../ide/how-to-create-item-templates.md)
- [Şablon parametreleri](../ide/template-parameters.md)
- [Şablonları özelleştirme](../ide/customizing-project-and-item-templates.md)
- [Visual Studio şablonları NuGet paketleri](/nuget/visual-studio-extensibility/visual-studio-templates)