---
title: XML verileriyle çalışırken güvenlik konuları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: fce2b708-1aef-454f-be59-52b76f359351
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 448396ebf8bf6318a22d7c6b05037d3ea43b0fd5
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65697123"
---
# <a name="security-considerations-when-working-with-xml-data"></a>XML Verileriyle Çalışırken Dikkat Edilecek Güvenlik Konuları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu konuda hakkında XML Düzenleyicisi'ni veya XSLT hata ayıklayıcısı ile çalışırken bilmeniz gereken güvenlik konuları açıklanmaktadır.  
  
## <a name="xml-editor"></a>XML Düzenleyicisi  
 XML Düzenleyicisi Visual Studio Metin Düzenleyicisi üzerinde temel alır. Kullanır <xref:System.Xml> ve <xref:System.Xml.Xsl> XML işlemlerin çoğunu işlemek için sınıflar.  
  
- XSLT dönüşümleri, yeni bir uygulama etki alanında yürütülür. XSLT dönüşümleri olan *korumalı*; diğer bir deyişle, kod erişimi güvenlik ilkesi bilgisayarınızın XSLT stil sayfası bulunduğu yeri üzerinde temel kısıtlı izinleri belirlemek için kullanılır. Örneğin, stil sayfaları tam güven ile çalışacak sabit diske kopyalanır, ancak bir Internet konumundan stil sayfaları en kısıtlı izinlere sahip.  
  
- <xref:System.Xml.Xsl.XslCompiledTransform> Sınıfı XSLT Microsoft Ara dili yürütme sırasında daha hızlı performans için derlemek için kullanılır.  
  
- XML Düzenleyicisi'ni ilk yüklendiğinde dış bir katalog dosyası konumuna işaret eden şemaları otomatik olarak yüklenir. <xref:System.Xml.Schema.XmlSchemaSet> Sınıfı şemaları derlemek için kullanılır. XML Düzenleyicisi ile birlikte gelen katalog dosyası bağlantılarını herhangi bir Dış şemalara sahip değil. Kullanıcının XML Düzenleyicisi şema dosyası indirir önce dış şema başvuru açıkça eklemeniz gerekir. HTTP indirmeyi devre dışı bırakılabilir aracılığıyla **çeşitli Araçlar Seçenekler** sayfası XML Düzenleyicisi için.  
  
- XML Düzenleyicisi kullanan <xref:System.Net> şemaları indirmek için sınıflar  
  
## <a name="xslt-debugger"></a>XSLT hata ayıklayıcısı  
 XSLT hata ayıklayıcı, Visual Studio yönetilen hata ayıklama motorunu kullanır ve gelen sınıflar <xref:System.Xml> ve <xref:System.Xml.Xsl> ad alanı.  
  
- XSLT hata ayıklayıcısı, koruma alanlı uygulama etki alanında her XSLT dönüşümü çalıştırır. Kod erişimi güvenlik ilkesi bilgisayarınızın XSLT stil sayfası bulunduğu yeri üzerinde temel kısıtlı izinleri belirlemek için kullanılır. Örneğin, stil sayfaları tam güven ile çalışacak sabit diske kopyalanır, ancak bir Internet konumundan stil sayfaları en kısıtlı izinlere sahip.  
  
- XSLT stil sayfası kullanılarak derlenmiş <xref:System.Xml.Xsl.XslCompiledTransform> sınıfı.  
  
- XSLT ifade değerlendiricisi yönetilen hata ayıklama altyapısı tarafından yüklenir. Yönetilen hata ayıklama altyapısı, tüm kod kullanıcının yerel bilgisayarınızdan çalıştırıldığını varsayar. Buna <xref:System.Xml.Xsl.XslCompiledTransform> sınıfı kullanıcının yerel bilgisayarına XSLT dosyasını indirir. Sınırlı izinler ile yeni bir uygulama etki alanındaki tüm XSLT dönüşümleri yürüterek, yürütme ayrıcalık yükselmesi oluşabilir olasılığı azaltılabilir  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uygulama Etki Alanları](https://msdn.microsoft.com/39e57d07-a740-4cd4-ae82-e119ea3856c1)
