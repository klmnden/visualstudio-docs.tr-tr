---
title: Tür tanımlarını görüntüleme
ms.date: 01/10/2018
ms.topic: conceptual
helpviewer_keywords:
- code editor, view definition
- go to definition
- peek definition
- type definition [Visual Studio]
- member definition [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2c5235bc19c1b06ec2cae26e3fcffb6a7d061c9b
ms.sourcegitcommit: 87d7123c09812534b7b08743de4d11d6433eaa13
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/01/2019
ms.locfileid: "57222928"
---
# <a name="view-type-and-member-definitions"></a>Görünüm türü ve üye tanımları

Geliştiriciler genellikle kendi kodlarında türler veya sınıf üyeleri kullandıkları için kaynak kod tanımlarını görüntülemek gerekir. Visual Studio'da **tanıma** ve **Özet tanım** özelliklerini kolayca tür veya üyenin tanımı görüntülemek etkinleştirin. Meta veri, kaynak kodu kullanılabilir durumda değilse, bunun yerine görüntülenir.

## <a name="go-to-definition"></a>Tanıma Git

**Tanıma** özellik bir türe veya üyeye kaynağına gider ve sonuç yeni bir sekmede açılır. Klavye kullanıcısıysanız yere tuşuna basın ve sembol adını içinde metin imleci yerleştirmeniz **F12**. Fare kullanıcısıysanız seçin **tanıma** sağ tıklama menüsünden veya kullanın **Ctrl tuşuna basıp** aşağıdaki bölümde anlatılan işlevi.

### <a name="ctrl-click-go-to-definition"></a>CTRL tuşunu tanımına Git

**CTRL**+**tıklayın** fare kullanıcılar hızlı erişim için bir kısayol **tanıma**. Semboller hale tıklanabilir bastığınızda **Ctrl** ve türe veya üyeye üzerine gelin. Sembol tanımını hızlıca gezinmek için basın **Ctrl** anahtar ve üzerine tıklayın. Bu kadar kolay!

![Fare tıklatın tanımı animasyon Git](../ide/media/click_gotodef.gif)

Fare tıklatın değiştirici tuş değiştirebilirsiniz **tanıma** giderek **Araçları** > **seçenekleri** > **metin düzenleyicisi**   >  **Genel**ve seçim **Alt** veya **Ctrl**+**Alt** gelen **değiştiricisi anahtar kullan** açılır. Fare tıklatın de devre dışı bırakabilirsiniz **tanıma** kaldırarak **tanıma gerçekleştirmek için fare tıklamasını etkinleştir** onay kutusu.

![Fare tıklatın etkinleştirme tanımına Git](../ide/media/editor_options_mouse_click_gotodef.png)

## <a name="peek-definition"></a>Tanıma göz at

**Özet tanım** özellik Düzenleyicisi'nde geçerli konumunuzu çıkmadan bir tür tanımı Önizleme olanak sağlar. Klavye kullanıcısıysanız yere tuşuna basın ve tür veya üye adı içindeki metin imleci yerleştirmeniz **Alt + F12**. Fare kullanıcısıysanız seçebileceğiniz **Özet tanım** sağ tıklatma menüsünden.

Etkinleştirmek için **Ctrl**+**tıklayın** işlevselliği, Git **Araçları** > **seçenekleri**  >   **Metin düzenleyici** > **genel**. Seçeneğini **tanımı Özet Görünümü'nde açın** tıklatıp **Tamam** kapatmak için **seçenekleri** iletişim kutusu.

![Fare tıklatın gözlem tanım seçeneği ayarlama](../ide/media/editor_options_peek_view.png)

Daha sonra basın **Ctrl** (veya hangi değiştirici tuşa seçili olduğundan **seçenekleri**), türe veya üyeye tıklayın.

![Özet tanım animasyon](../ide/media/peek_definition.gif)

Başka bir açılan pencere tanımından Özet, daire ve açılan menüsü görünen okları kullanarak gezinebileceğiniz bir içerik haritası yol başlatın.

Daha fazla bilgi için [nasıl yapılır: Görüntüleme ve Özet tanım (Alt + F12) kullanarak kod düzenleme](how-to-view-and-edit-code-by-using-peek-definition-alt-plus-f12.md).

## <a name="view-metadata-as-source-code-c"></a>Kaynak kodu olarak meta verileri görüntüleme (C#)

Tanımı görüntülediğinizde C# türleri veya üyeleri kaynak kodu kullanılabilir değil, meta veriler görüntüleniyor. Türleri ve üyeleri, ancak kendi uygulamalarını bildirimlerini görebilirsiniz.

Çalıştırdığınızda **tanıma** veya **Özet tanım** kaynak kodu kullanılamıyor, bir öğenin bu öğeye ait meta verilerin, kaynak kodu görüntülenen bir görünüm içeren sekmeli belge komutu Kod Düzenleyicisi'nde görünür. Türün adını ve ardından **[meta verilerden]**, belgenin sekmesinde görünür.

Örneğin çalıştırırsanız, **tanıma** komutunu <xref:System.Console>, meta verileri <xref:System.Console> Kod Düzenleyicisi görünür C# kaynak kodu. Kod bildiriminden benzer, ancak bir uygulama göstermez.

![Kaynak olarak Meta Veriler](../ide/media/metadatasource.png)

> [!NOTE]
> Çalıştırılacak çalıştığınızda **tanıma** veya **Özet tanım** komut türleri veya iç olarak işaretlenmiş üyeleri için Visual Studio görüntülemez meta verilerinin bağımsız olarak, kaynak kodu başvuru bütünleştirilmiş kod veya arkadaş olur.

### <a name="view-decompiled-source-definitions-instead-of-metadata-c"></a>Kaynak koda dönüştürülmüş kaynak tanımları yerine meta verileri görüntüleme (C#)

Ayarlayabileceğiniz bir seçenek tanımı görüntülediğinizde, kaynak koda dönüştürülmüş kaynak kodu görmek için bir C# tür veya üye, kaynak kodu kullanılamaz. Bu özelliği etkinleştirmek için seçin **Araçları** > **seçenekleri** menü çubuğundan. Ardından, **metin düzenleyici** > **C#** > **Gelişmiş**seçip **kaynak koda dönüştürülmüş kaynaklara gezintiyi etkinleştir** .

![Kaynak koda dönüştürülmüş tanımını görüntüleme](media/go-to-definition-decompiled-sources.png)

> [!NOTE]
> Visual Studio metot gövdeleri yetenek ılspy kullanarak yeniden oluşturur. Bu özellik, erişim ilk kez ticari marka yasaları ve yazılım lisans ve telif hakkı ile ilgili yasal Sorumluluklar kabul gerekir.

## <a name="see-also"></a>Ayrıca bkz.

- [Kod gidin](../ide/navigating-code.md)
- [Nasıl yapılır: Görüntüleme ve Özet tanım (Alt + F12) kullanarak kod düzenleme](how-to-view-and-edit-code-by-using-peek-definition-alt-plus-f12.md)