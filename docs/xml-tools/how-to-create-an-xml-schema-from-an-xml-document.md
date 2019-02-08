---
title: 'Nasıl yapılır: XML Belgesinden XML Şeması Oluşturma'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 1d6700a9-fd67-4794-8997-399589e99bec
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ebea3b20bc606ec82529e4a9b2a547d6a44fc905
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55953795"
---
# <a name="how-to-create-an-xml-schema-from-an-xml-document"></a>Nasıl yapılır: Bir XML belgesinden XML şeması oluşturma

XML Düzenleyicisi, bir XML Şeması Tanım Dili (XSD) şeması bir XML belgesinden oluşturmanıza olanak sağlar. Örnek XML Belge Şeması aşağıdaki şekilde nasıl oluşturulacağını belirler:

-   XML belgesi bir şeması yok veya belge türü tanımı (DTD'nin) ilişkili varsa, XML belgesi verileri yeni bir XML şema çıkarsanacak kullanılır.

-   XML belgesi ilişkili bir DTD'nin içeriyorsa, karşılık gelen bir XML şeması için dış DTD'nin ve iç alt dönüştürülür.

-   XML belgesi bir satır içi XML verileri azaltılmış (XDR) şema içeriyorsa, karşılık gelen bir XML şemasına XDR şeması dönüştürülür.

Oluşturulan şemaları, daha sonra XML belgesi için IntelliSense sağlamak için kullanılır.

Şema çıkarımı altyapısının hakkında daha fazla bilgi için bkz: [XML şemasından çıkarım yapma](/dotnet/standard/data/xml/inferring-an-xml-schema).

## <a name="to-create-an-xml-schema"></a>Bir XML şeması oluşturmak için

1.  XML örnek belge ile XML Düzenleyicisi'ni yükleyin.

2.  Tıklayın **Create Schema** düğmesini **araç**.

     Bir XML Şeması belgesi oluşturulup XML örneği belgesinde bulunan her ad alanı için açılır. Her şema geçici çeşitli dosya olarak açılır.

     Şemalar, projenize eklenir veya atılan diske kaydedildi.

    > [!NOTE]
    >  **Create Schema** komutu kısayol menüsünde bulunan XML Düzenleyicisi'nin altında ve ayrıca **XML** menüsü.

## <a name="see-also"></a>Ayrıca bkz.

- [XML Düzenleyicisi](../xml-tools/xml-editor.md)