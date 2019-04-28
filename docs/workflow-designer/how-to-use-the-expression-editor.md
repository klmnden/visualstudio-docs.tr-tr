---
title: 'İş Akışı Tasarımcısı - nasıl yapılır: İfade Düzenleyicisini Kullanma'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- System.Activities.Presentation.View.ExpressionTextBox.UI
ms.assetid: b5f961dd-6dda-41a9-9cae-0383d479ef3d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ce46f1db900aa5c37b49a1cc228290d7d99d29a2
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62949545"
---
# <a name="how-to-use-the-expression-editor"></a>Nasıl yapılır: İfade Düzenleyicisini Kullanma

İfade Düzenleyicisi'ni girin ve ifadeleri değerlendirmek için kullanılan birçok iş akışı etkinliklerinde bir iş akışı Tasarımcısı denetimidir. İfade Düzenleyicisi düzenleme deneyimi de dahil olmak üzere IntelliSense, renklendirme, tam özellikli bir IDE sağlar Paramınfo, diğer özellikler arasında hata ilişkilendirmelerini. Bunu girildikten sonra derleyici ifadesini doğrular. İfade geçersizse, bir hata simgesi görüntülenir. Düzenleyici olarak de açılabilir bir **ifade Düzenleyicisi** iletişim kutusu.

Değişmez değerler veya Visual Basic kodunu bağımsız değişkenler veya özellikleri bağlı ifadelerdir. Yeni bir değer yield işlemleriyle birlikte değeri öğeleri (örneğin, değişkenleri, sabitleri, sabit değerleri, özellikleri) içerirler. İfadeler, C# kullanarak bir programda uygulaması olsa bile VB.NET söz dizimini kullanarak yazılır. Büyük/küçük harf önemli değildir, tek bir eşittir kullanarak karşılaştırma gerçekleştirilir yani oturum ("=" "==" yerine), Boole işleçleri sözcüklerdir "ve" ve "veya" sembolleri yerine "& &" ve "||", ve **hiçbir şey** kullanılır yerine **null**. İfadeler ve Visual Basic'de işleçler hakkında daha fazla bilgi ve bazı örnekler için bkz: [işleçler ve ifadeler Visual Basic'te](/previous-versions/visualstudio/visual-studio-2010/a1w3te48(v=vs.100)).

**İfade Düzenleyicisi** gibi davranır:

- Odağı ifade Düzenleyicisi üzerinde değilse, normal bir TextBlock denetimi gibi görünüyor.

- Odağı ifade düzenleyicisini olduktan sonra görünür ve ifade Düzenleyicisi denetimi gibi davranır. Odağı kaybettiğinde sonra ifade Düzenleyicisi gibi normal bir TextBlock tekrar görünür.

- Daha sonra yeniden barındırılan iş akışı Tasarımcısı'nda ifade Düzenleyicisi üzerinde odaklanmak, bir metin kutusu gibi davranır. Yeniden barındırılan iş akışı Tasarımcısı'nda odağı kaybettiğinde ifade Düzenleyicisi gibi normal bir TextBlock yeniden görünür.

> [!NOTE]
> IntelliSense için ifade Düzenleyicisi yalnızca Visual Studio içinde kullanılabilir. Visual Studio hem yeniden barındırılan senaryoları derleyici ifade girildiği ve ifade geçersiz bir hata simgesi ifade düzenleyicisini görüntüler sonra doğrular.

## <a name="use-the-expression-editor"></a>İfade Düzenleyicisini Kullanma

1. Visual Studio'da, yeni veya var olan iş akışı projesi açın.

2. Ekleme, örneğin, <xref:System.Activities.Statements.Assign> etkinlik akışınıza.

    > [!NOTE]
    > Birden çok iş akışı etkinlikleri ifade düzenleyicileri vardır. İfade TextBlock'lar değişken tasarımcısını, bağımsız değişken tasarımcısını ve dinamik bağımsız değişken tasarımcısını da görünür. <xref:System.Activities.Statements.Assign> Etkinliği, örnek olarak kullanılır.

3. Sol ifade Düzenleyicisi için etkinlik Tasarımcısı'nda <xref:System.Activities.Statements.Assign> etkinlik.

     Gri Filigran dizeleri  **\<için >** ve  **\<zadejte Výraz jazyka vb. >** varsayılan ifade Düzenleyicilerde metin dizelerini içindir <xref:System.Activities.Statements.Assign> etkinlik.

4. İfadeniz girin. Bir dize girin, dize etrafında tırnak işareti koymak emin olun. İfade bağımsız değişkeni bir değişkene bağlamak isterseniz, tırnak işaretleri bırakın.

     İşiniz bittiğinde, bir bölge ya da alanı dışında ifade odağı tasarımcının başka bir parçası için Düzenleyici'yi seçin. Odağı kaydırma, daha önce açıklandığı şekilde ifadeyi doğrulamak derleyicinin neden olur.

     Alternatif bir yol girin veya bir ifade düzenlemek için özellik kılavuzunda özellik adının yanındaki üç noktaya tıklayın sağlamaktır. Üç noktayı seçtiğinizde açılır **ifade Düzenleyicisi** bir iletişim kutusu olarak.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Activities.Presentation.View.ExpressionTextBox>