---
title: 'İş Akışı Tasarımcısı - nasıl yapılır: Bağımsız Değişken Tasarımcısını Kullanma'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- System.Activities.Presentation.View.ArgumentDesigner.UI
- System.Activities.Presentation.View.DesignTimeArgument.UI
ms.assetid: 64813fd5-1ea1-499a-98b4-ab2a44b7ee5e
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2f32228de6486c7e2093175bcd57d698a881ab7f
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60115815"
---
# <a name="how-to-use-the-argument-designer"></a>Nasıl yapılır: Bağımsız Değişken Tasarımcısını Kullanma

.NET Framework'ün önceki sürümleriyle karşılaştırıldığında, bağımsız değişken tasarımcısını, veri ekleme çıkarma bir etkinlik akışı izin vermek kolaylaştırır. Tasarımcı tıklayarak erişilen **bağımsız değişkenleri** tasarım tuvalin sol alt köşesindeki düğme. Tasarımcı, bir tablo biçiminde görünür ve her bir sütun üst bilgileri dışında sıralanabilir bağımsız değişkenlerinin listesi içeren **varsayılan değer** sütun. Her bağımsız değişken adı, / out/içinde-out/özellik yönü, türü ve varsayılan ifade değeri (varsa) içerir. Adı ve varsayılan ifade değeri düzenlenebilir metin alanları ve türü ve Yön açılan listeler. Daha fazla bilgi için [değişkenleri ve bağımsız değişkenler (.NET)](/dotnet/framework/windows-workflow-foundation/variables-and-arguments).

## <a name="to-create-a-new-argument"></a>Yeni bir değişken oluşturmak için

1. Bir iş akışı veya etkinlik çözümünü Visual Studio'da açın.

2. Bağımsız değişkenler Tasarımcısı'nı tıklatarak **bağımsız değişkenleri** tasarım tuvalin sol alt köşesindeki düğme. Bağımsız değişken tasarımcısını görünür.

3. Etiketli boş satırı tıklatın **bağımsız değişken oluşturma**. Bu aşağıdaki varsayılan değerleri kullanarak yeni bir değişken ile yeni bir satır ekler: argumentx için **adı** x benzersiz bağımsız değişken adları oluşturmak için otomatik olarak artırılır 1 başlangıç değeri bir tamsayı olduğu **içinde**  için **yönü**, ve **dize** için **bağımsız değişken türü**. Hiçbir değer için eklenen **varsayılan değer**. İş akışı tasarım işlemi sırasında herhangi bir zamanda bu değerleri değiştirebilirsiniz.

    > [!NOTE]
    > Bir değişkeni silmek için bağımsız değişken tıklayarak seçin ve tuşuna **Sil** anahtarı.

## <a name="see-also"></a>Ayrıca bkz.

- [İş Akışı Tasarımcısını Kullanma](developing-applications-with-the-workflow-designer.md)
- [Değişkenler ve Bağımsız Değişkenler](/dotnet/framework/windows-workflow-foundation/variables-and-arguments)