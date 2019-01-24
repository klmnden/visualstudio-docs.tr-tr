---
title: 'Nasıl yapılır: Bir XML belgesinden XML şeması oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: 1d6700a9-fd67-4794-8997-399589e99bec
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 50e601d03901484ed6e759fb336b1effa5b37841
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54773259"
---
# <a name="how-to-create-an-xml-schema-from-an-xml-document"></a>Nasıl yapılır: XML Belgesinden XML Şeması Oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
XML Düzenleyicisi, bir XML Şeması Tanım Dili (XSD) şeması bir XML belgesinden oluşturmanıza olanak sağlar. Örnek XML Belge Şeması aşağıdaki şekilde nasıl oluşturulacağını belirler:  
  
- XML belgesi bir şeması yok veya belge türü tanımı (DTD'nin) ilişkili varsa, XML belgesi verileri yeni bir XML şema çıkarsanacak kullanılır.  
  
- XML belgesi ilişkili bir DTD'nin içeriyorsa, karşılık gelen bir XML şeması için dış DTD'nin ve iç alt dönüştürülür.  
  
- XML belgesi bir satır içi XML verileri azaltılmış (XDR) şema içeriyorsa, karşılık gelen bir XML şemasına XDR şeması dönüştürülür.  
  
  Oluşturulan şemaları, daha sonra XML belgesi için IntelliSense sağlamak için kullanılır.  
  
  Şema çıkarımı altyapısının hakkında daha fazla bilgi için bkz: [XML şemasından çıkarım yapma](http://msdn.microsoft.com/library/b18e7ffd-3c04-482d-9934-ba2f6a59b2c9).  
  
### <a name="to-create-an-xml-schema"></a>Bir XML şeması oluşturmak için  
  
1.  XML örnek belge ile XML Düzenleyicisi'ni yükleyin.  
  
2.  Tıklayın **Create Schema** düğmesini **araç**.  
  
     Bir XML Şeması belgesi oluşturulup XML örneği belgesinde bulunan her ad alanı için açılır. Her şema geçici çeşitli dosya olarak açılır.  
  
     Şemalar, projenize eklenir veya atılan diske kaydedildi.  
  
    > [!NOTE]
    >  **Create Schema** komutu kısayol menüsünde bulunan XML Düzenleyicisi'nin altında ve ayrıca **XML** menüsü.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [XML Düzenleyicisi](../xml-tools/xml-editor.md)
