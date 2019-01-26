---
title: 'İş Akışı Tasarımcısı - nasıl yapılır: Değişken Tasarımcısını Kullanma'
ms.date: 11/04/2016
ms.topic: conceptual
ms.prod: visual-studio-dev15
f1_keywords:
- System.Activities.Presentation.View.DesignTimeVariable.UI
ms.assetid: 0318dfb0-bf8f-4f92-9b86-ae4c1b2161ad
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f6d50fa27111cfb7f58c39cb29e7ff34038a1b6e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54959206"
---
# <a name="how-to-use-the-variable-designer"></a>Nasıl yapılır: Değişken Tasarımcısını Kullanma

Değişken tasarımcısını kullanmak için değişkenler veri bağlama senaryoları ve koşul deyimlerini oluşturmak için kullanılır. Tasarımcı tıklayarak erişilen **değişkenleri** tasarım tuvalin sol alt köşesindeki düğme. Tasarımcı, bir tablo biçiminde görünür ve her bir sütun üst bilgileri dışında sıralanabilir değişkenlerin bir listesi içeren **varsayılan** sütun. Her bir değişken adı, değişken türü, kapsamı ve varsayılan değer (varsa) içerir. Ad ve varsayılan değer düzenlenebilir metin alanları ve türüne ve kapsamına açılan listeler. Kapsam değişken tasarımcısını çağrıldığında, seçilen etkinliğidir. Bir değişken seçimi kapsamında oluşturulamıyorsa, kapsamı en yakın üst etkinliği değişkenleri kapsamında oluşturulmasına izin veren seçimin varsayılacaktır. Daha fazla bilgi için [değişkenleri ve bağımsız değişkenler (.NET)](/dotnet/framework/windows-workflow-foundation/variables-and-arguments).

 Sıralama düzenini kullanıcı açıkça sıralama denetimlerden birini kullanır, kapatır ve değişken tasarımcısını yeniden açana veya başka bir değişken oluşturur kadar uygulanmaz.

## <a name="to-create-a-new-variable"></a>Yeni bir değişken oluşturmak için

1.  Bir iş akışı veya etkinlik çözümünü Visual Studio'da açın.

2.  Tasarım tuvalde akışınızda bir etkinlik seçin.

3.  Değişken tasarımcısını tıklatarak **değişkenleri** tasarım tuvalin sol alt köşesindeki düğme. Değişken tasarımcısını görünür.

4.  Etiketli boş satırı tıklatın **oluşturma değişken**. Bu aşağıdaki varsayılan değerleri kullanarak yeni bir değişken ile yeni bir satır ekler: variablex için **adı** x benzersiz değişken adları oluşturmak için otomatik olarak artırılır 1 başlangıç değeri bir tamsayı olduğu  **Dize** için **değişken türü**, ve **dizisi** için **kapsam**. Hiçbir değer için eklenen **varsayılan**. İş akışı tasarım işlemi sırasında herhangi bir zamanda bu değerleri değiştirebilirsiniz.

    > [!NOTE]
    > Bir değişkeni silmek için değişken tıklayarak seçin ve tuşuna **Sil** anahtarı.

## <a name="see-also"></a>Ayrıca bkz.

- [İş Akışı Tasarımcısını Kullanma](developing-applications-with-the-workflow-designer.md)
- [Değişkenler ve Bağımsız Değişkenler](/dotnet/framework/windows-workflow-foundation/variables-and-arguments)
- [Nasıl yapılır: Bağımsız değişken Tasarımcısını kullanma](../workflow-designer/how-to-use-the-argument-designer.md)