---
title: XML Verileriyle Çalışırken Dikkat Edilecek Güvenlik Konuları
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: fce2b708-1aef-454f-be59-52b76f359351
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5fe4ec69f879478566cce8d077bb66b34da86f3d
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926769"
---
# <a name="security-considerations-when-working-with-xml-data"></a>XML verileriyle çalışırken güvenlik konuları

Bu konuda, XML Düzenleyicisi veya XSLT hata ayıklayıcıyla çalışırken bilmeniz gereken güvenlik sorunları ele alınmaktadır.

## <a name="xml-editor"></a>XML düzenleyicisi

XML Düzenleyicisi, Visual Studio metin düzenleyiciyi temel alır. XML işlemlerinin çoğunu işlemek <xref:System.Xml> için <xref:System.Xml.Xsl> ve sınıflarını kullanır.

- XSLT dönüştürmeleri yeni bir uygulama etki alanında yürütülür. XSLT dönüşümleri *korumalı*değildir; diğer bir deyişle, bilgisayarınızın kod erişimi güvenlik ilkesi, XSLT stil sayfasının bulunduğu yere göre kısıtlanmış izinleri belirlemekte kullanılır. Örneğin, bir Internet konumundan stil sayfaları en kısıtlı izinlere sahiptir, ancak sabit sürücünüze kopyalanmış stil sayfaları tam güvenle çalışır.

- <xref:System.Xml.Xsl.XslCompiledTransform> Sınıfı, yürütme sırasında daha hızlı performans için XSLT 'yi Microsoft ara diline derlemek için kullanılır.

- Katalog dosyasındaki bir dış konuma işaret eden şemalar, XML Düzenleyicisi ilk kez yüklendiğinde otomatik olarak indirilir. <xref:System.Xml.Schema.XmlSchemaSet> Sınıfı, şemaları derlemek için kullanılır. XML Düzenleyicisi ile birlikte gelen Katalog dosyası herhangi bir dış şemaya yönelik bağlantılara sahip değildir. XML Düzenleyicisi şema dosyasını indirmeden önce, kullanıcının dış şemaya açıkça bir başvuru eklemesi vardır. HTTP indirme, XML Düzenleyicisi için **çeşitli Araçlar Seçenekler** sayfası aracılığıyla devre dışı bırakılabilir.

- XML Düzenleyicisi şemaları indirmek için <xref:System.Net> sınıfları kullanır

## <a name="xslt-debugger"></a>XSLT hata ayıklayıcısı

XSLT hata ayıklayıcı, <xref:System.Xml> ve <xref:System.Xml.Xsl> ad alanından Visual Studio tarafından yönetilen hata ayıklama altyapısını ve sınıfları kullanır.

- XSLT hata ayıklayıcısı her XSLT dönüşümünü bir korumalı uygulama etki alanında çalıştırır. Bilgisayarınızın kod erişimi güvenlik ilkesi, XSLT stil sayfasının bulunduğu yere göre kısıtlanmış izinleri belirlemekte kullanılır. Örneğin, bir Internet konumundan stil sayfaları en kısıtlı izinlere sahiptir, ancak sabit sürücünüze kopyalanmış stil sayfaları tam güvenle çalışır.

- XSLT stil sayfası <xref:System.Xml.Xsl.XslCompiledTransform> sınıfı kullanılarak derlenir.

- XSLT ifade değerlendirici yönetilen hata ayıklama altyapısı tarafından yüklenir. Yönetilen hata ayıklama altyapısı, tüm kodun kullanıcının yerel bilgisayarından çalıştırıldığını varsayar. Buna uygun olarak <xref:System.Xml.Xsl.XslCompiledTransform> , sınıfı XSLT dosyasını kullanıcının yerel bilgisayarına indirir. Yürütme ayrıcalığının bir yükseltmesinde, kısıtlanmış izinlerle yeni bir uygulama etki alanındaki tüm XSLT dönüştürmeleri yürütülerek hafiflemesinin oluşma olasılığı

## <a name="see-also"></a>Ayrıca bkz.

- [Uygulama etki alanları](/dotnet/framework/app-domains/application-domains)