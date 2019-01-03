---
title: Araç Kutusu Öğelerini, WPF Bileşenlerini Seçme
ms.date: 06/21/2017
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- vs.chooseitems.wpfcomponents
helpviewer_keywords:
- WPF Components tab, Choose Toolbox Items dialog box
- Choose Toolbox Items dialog box, WPF Components tab
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 22cc50089a21f1ed836200f03a4681553bc5e94b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53990639"
---
# <a name="choose-toolbox-items-wpf-components"></a>Araç kutusu öğelerini, WPF bileşenlerini seçme

Bu sekme, **araç kutusu öğelerini Seç** iletişim kutusu, yerel bilgisayarınızda Windows Presentation Foundation (WPF) kullanılabilir denetimleri bir listesini görüntüler. Bu listeyi görüntülemek için seçin **araç kutusu öğelerini Seç** gelen **Araçları** görüntülenecek menü **araç kutusu öğelerini Seç** iletişim kutusunu ve ardından kendi **WPF Bileşenleri** sekmesi. Listelenen bileşenleri sıralamak için herhangi bir sütun başlığını seçin.

- Bir bileşen yanındaki onay kutusunu seçtiğinizde, söz konusu bileşen için bir simge görüntülenir **araç kutusu**.

    > [!TIP]
    > Düzenleme için açık olan proje belgeye bir WPF denetimi eklemek için sürükleyin, **araç kutusu** Tasarım görünümü yüzeyine simgesi. Varsayılan işaretleme ve kod bileşeni için projenize değiştirmek hazır eklenir. Daha fazla bilgi için [araç kutusu](../../ide/reference/toolbox.md).

- Bir bileşen yanındaki onay kutusunu temizlendiğinde, karşılık gelen simgeyi kaldırılacak **araç kutusu**.

    > [!NOTE]
    > Bunlar için simgeler görüntülenir olup olmadığını bilgisayarınızda yüklü .NET Framework bileşenlerini sunulmaya **araç kutusu**.

Sütunlarda **WPF bileşenleri** sekmesine aşağıdaki bilgileri içerir:

**Ad**

WPF denetimleri, girdileri bilgisayarınızın kayıt defterinde mevcut adlarını listeler.

**Namespace**

Hiyerarşisini görüntüler [.NET Framework sınıf API](/dotnet/api/?view=netframework-4.7) bileşeni yapısını tanımlayan ad. Bilgisayarınızda yüklü her .NET Framework ad alanı içinde kullanılabilir bileşenleri listelemek için bu sütun sıralama.

**Derleme adı**

Her bileşen için ad alanı içeren bir .NET Framework derlemesinin adını görüntüler. Bilgisayarınızda yüklü her .NET Framework derlemesi içindeki ad alanlarını listelemek için bu sütun sıralama.

**Dizin**

.NET Framework derlemesinin konumunu görüntüler. Genel Derleme Önbelleği tüm derlemeler için varsayılan konumdur. Genel Derleme Önbelleği hakkında daha fazla bilgi için bkz: [derlemeler ve genel derleme önbelleği ile çalışma](/dotnet/framework/app-domains/working-with-assemblies-and-the-gac).

## <a name="uielement-list"></a>UIElement Listesi

### <a name="filter"></a>Filtrele

Metin kutusunda sağladığınız dizenin göre WPF denetim listesini filtreler. Tüm eşleşmeleri herhangi birinden dört sütun gösterilmektedir.

**Temizle**

Filtre dizesi temizler.

**Göz atma**

Açılır **açık** iletişim kutusunda, WPF denetimleri içeren derlemeler gezinmenize olanak tanır. Hangi genel derleme önbelleğinde bulunmayan derlemeler yüklemek için bunu kullanın.

**Dil**

Seçili WPF denetimi içeren bütünleştirilmiş kodun yerelleştirilmiş dilini gösterir.

## <a name="limitations"></a>Sınırlamalar

Özel denetim ekleme veya <xref:System.Windows.Controls.UserControl> araç kutusuna aşağıdaki sınırlamalara sahiptir:

- Yalnızca güncel proje dışında tanımlanmış özel denetimler için çalışır.

- Doğru sürüm için hata ayıklama veya sürüm hata ayıklama çözüm yapılandırması değiştirdiğinizde güncelleştirmez. Başvuru yapılan proje başvurusunun değildir, ancak bunun yerine derleme diskte içindir olmasıdır. Denetim, hata ayıklama'dan sürümüne değiştirdiğinizde geçerli çözümün bir parçası ise, projenizin hata ayıklama sürümü denetimi başvurmak devam eder.

Ayrıca, tasarım zamanı meta verileri özel denetim ve bu meta veriler için uygulanırsa belirtir <xref:Microsoft.Windows.Design.ToolboxBrowsableAttribute> ayarlanır `false`, denetimin araç kutusunda görünmüyor.

Ad alanını ve derlemeyi denetiminizin eşleyerek denetimlerinizi XAML görünümünde doğrudan başvurabilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

- [Araç Kutusu](../../ide/reference/toolbox.md)
- [WPF Kullanmaya Başlarken](../../designers/getting-started-with-wpf.md)
