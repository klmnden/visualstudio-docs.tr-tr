---
title: XML şeması oluşturma
ms.date: 03/05/2019
ms.topic: conceptual
ms.assetid: 1d6700a9-fd67-4794-8997-399589e99bec
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0e93155f230ee4a564116f5d1357a97923706c36
ms.sourcegitcommit: 3ca33862c1cfc3ccb83de3e95f1e69e860ab143a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57526135"
---
# <a name="how-to-create-an-xml-schema-from-an-xml-document"></a>Nasıl yapılır: Bir XML belgesinden XML şeması oluşturma

XML Düzenleyicisi, bir XML Şeması Tanım Dili (XSD) şeması bir XML belgesinden oluşturmanızı sağlar. XML dosyası şeması aşağıdaki şekilde nasıl oluşturulacağını belirler:

- XML belgesi bir şeması yok veya belge türü tanımı (DTD'nin) ilişkili varsa, XML belgesi verileri yeni bir XML şema çıkarsanacak kullanılır.

- XML belgesi ilişkili bir DTD'nin içeriyorsa, karşılık gelen bir XML şeması için dış DTD'nin ve iç alt dönüştürülür.

- XML belgesi bir satır içi XML verileri azaltılmış (XDR) şema içeriyorsa, karşılık gelen bir XML şemasına XDR şeması dönüştürülür.

Oluşturulan şemaları, daha sonra XML dosyası için IntelliSense sağlamak için kullanılır.

Şema çıkarımı altyapısının hakkında daha fazla bilgi için bkz: [bir XML şeması tanım Çıkarsama](/dotnet/standard/data/xml/inferring-an-xml-schema).

## <a name="to-create-an-xml-schema"></a>Bir XML şeması oluşturmak için

1. Bir XML dosyasını Visual Studio'da açın.

2. Menü çubuğunda, **XML** > **Create Schema**.

   Bir XML Şeması belgesi oluşturulup XML dosyasında bulunan her ad alanı için açılır. Her şema geçici çeşitli dosya olarak açılır. Şemalar, projenize eklenir veya atılan diske kaydedildi.

## <a name="see-also"></a>Ayrıca bkz.

- [XML Düzenleyicisi](../xml-tools/xml-editor.md)