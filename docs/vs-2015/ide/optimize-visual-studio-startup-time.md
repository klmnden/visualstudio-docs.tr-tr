---
title: Başlatma süresini iyileştirme | Microsoft Docs
ms.date: 11/15/2016
ms.topic: conceptual
helpviewer_keywords:
- startup time [Visual Studio]
- optimizing startup time [Visual Studio]
- speed up start time [Visual Studio]
ms.assetid: d1508121-8499-4084-8eb5-fa89fa7b17d3
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 98d54f1e43090e8e1cacf8aecac9eebd18ffcbd7
ms.sourcegitcommit: 3201da3499051768ab59f492699a9049cbc5c3c6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/22/2019
ms.locfileid: "58355376"
---
# <a name="optimize-visual-studio-startup-time"></a>Visual Studio Başlangıç süresini iyileştirme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İdeal olarak, Visual Studio her zaman mümkün olan en kısa sürede başlatılır. Bunların başlangıçta otomatik olarak yüklemek için ancak Visual Studio uzantıları ve açık aracı penceresi başlangıç zamanı olumsuz etkileyebilir. **Visual Studio performansını Yönet** penceresi yalnızca hangi uzantıları ve özellikleri, Visual Studio Başlangıç süresini etkileyen görmenizi sağlar, ancak ayrıca hızlı bir şekilde nasıl hakkında daha fazla denetime sahip yükleme davranışlarını belirlemenize olanak tanır Visual Studio başlatılır.

## <a name="control-startup-behavior"></a>Başlangıç davranışını denetimi

Başlangıç zamanı, Visual Studio 2017 genişletme önlemek ve daha sonra uzantıları-isteğe bağlı-yüklemede yaklaşımı kullanarak başlatma sırasında yükleme önlemek için. Bu, hemen Visual Studio başlatmaz, bunun yerine bir gerektiğinde temelinde başlatma işleminden sonra zaman uyumsuz olarak açmak sonra uzantıları açmayın anlamına gelir. Ayrıca, önceki bir Visual Studio oturumu açık sol araç pencereleri başlangıç zamanını yavaşlatabileceği için Visual Studio Başlangıç süresini etkileyen önlemek için daha akıllı bir şekilde araç pencereleri açılır.

Visual Studio yavaş başlatma algılarsa, yavaşlama neden olan uzantı veya araç penceresinin için uyarı bir açılır ileti görüntülenir. İleti bir bağlantı da sağlar. **Visual Studio performansını Yönet** iletişim kutusunda, başlangıç performansı etkileyen uzantıları ve araç pencerelerini listeler. Bu iletişim kutusunu başlatma performansını artırmak için uzantı ve araç penceresi ayarlarını değiştirmenize olanak tanır.

![-Visual Studio performansını Yönet açılan](../ide/media/vside-perfdialog-popup.PNG "Visual Studio performansını Yönet - açılan menüsü")

**Visual Studio performansını Yönet** iletişim kutusunda iki kategorisi vardır: **Uzantıları** ve **aracı Windows**.

### <a name="control-extensions"></a>Denetim uzantıları
Bir uzantıyı Visual Studio Başlangıç yavaşlatıyor uzantısı görünür **Visual Studio performansını Yönet iletişim** kutusuna uzantı türleri birini seçtiğinizde. Başlangıç zamanı üzerindeki etkisi (altında listelenen **etkisi** bölümü) olan edilemeyecek kadar yüksek, her zaman başlangıçta uzantısı seçerek devre dışı bırakmak seçebileceğiniz **devre dışı** düğmesi. Uzantı sonraki oturumlar için Uzantı Yöneticisi'ni veya Visual Studio performansını Yönet iletişim kutusunu kullanarak yeniden etkinleştirebilirsiniz.

![Visual Studio performansını - uzantıları Yönet](../ide/media/vside-perfdialog-extensions.PNG "Visual Studio performansını Yönet - uzantıları")

Başlangıç uzantılarını yanı sıra yük çözümleri yüklediğinizde veya bir kullanıcı yazdığında uzantıları da devre dışı bırakabilirsiniz. Yalnızca ilişkili uzantıların listesini görmek için senaryo seçin.

### <a name="control-tool-windows"></a>Denetimi Araç pencereleri
Araç penceresi Visual Studio Başlangıç yavaşlatıyor, varsayılan davranışını (size hiçbir avantajı başlangıç hızı sağlar) adresindeki bırakın seçebilirsiniz veya iki davranışları birini seçerek davranışını geçersiz kılabilirsiniz:

- **Başlangıçta pencere gösterme:** Bu seçeneği belirlerseniz, Visual Studio'da açtığınızda belirtilen araç penceresi her zaman içinde önceki bir oturum açma sol bile kapatılacak. Araç penceresi menüsünden açabilirsiniz.
- **Başlangıçta pencereyi otomatik gizle:** Araç penceresini önceki bir oturumda açık bırakılırsa, bu seçeneğin seçilmesi araç penceresi başlatma önlemek için aracının pencere grubu başlangıçta daraltın. Araç penceresi hala kullanılabilir ancak Visual Studio Başlangıç süresini artık olumsuz etkiler çünkü araç penceresi genellikle kullanırsanız, iyi bir seçimdir.

![Araç pencereleri - Visual Studio performansını Yönet](../ide/media/vside-perfdialog-toolwindows.PNG "Visual Studio performansını Yönet - araç pencereleri")

Daha sonra fikrinizi değiştirirseniz, bu seçeneklerin hiçbirini döndürebilirsiniz **Visual Studio performansını Yönet** iletişim kutusu. Açmak için **Visual Studio performansını Yönet** Seç iletişim kutusu, menü çubuğunda, **yardımcı**, **Visual Studio performansını Yönet**.
