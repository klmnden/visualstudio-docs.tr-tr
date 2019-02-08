---
title: Bir yöntem çağrılarını bulun
ms.date: 05/18/2018
ms.topic: reference
f1_keywords:
- VS.CallHierarchy
helpviewer_keywords:
- Call Hierarchy
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ad95d1c48992b8ecac6715db41aa9d85791999bb
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55910370"
---
# <a name="view-call-hierarchy"></a>Çağrı hiyerarşisini görüntüle

Kodunuz için çağrı hiyerarşisini görüntüleyerek tüm çağrıları için ve bazen seçili yöntemi, özelliği veya Oluşturucu gidebilirsiniz. Bu, daha iyi kodun nasıl aktığını anlamak ve kod değişikliklerinin etkilerini değerlendirilecek sağlar. Kod yöntem çağrıları ve ek giriş noktaları kod karmaşık zincirleri görüntülemek için çeşitli düzeylerde inceleyebilirsiniz. Bu, tüm olası yürütme yolları olarak keşfetmenize olanak sağlar.

Visual Studio'da tasarım zamanında bir çağrı hiyerarşisini görüntüleyebilirsiniz. Bu, bir kesme noktası ayarlayın ve çalışma zamanı çağrı yığınını görmek için hata ayıklayıcıyı başlatmak zorunda olmadığınız anlamına gelir.

## <a name="use-the-call-hierarchy-window"></a>Çağrı hiyerarşisi penceresi kullanma

Görüntülenecek **çağrı hiyerarşisi** penceresinde Kod düzenleyicisinde bir yöntemi, özelliği veya oluşturucu çağrısı adına sağ tıklayın ve ardından **çağrı hiyerarşisini**.

Üye adı bir ağaç görünümü bölmesinde görünür **çağrı hiyerarşisi** penceresi. Üye düğümünü genişletirseniz **çağrıları için** *üye adı*ve C++ için **gelen çağrıları** *üye adı*, düğümlerinde görünür.

C++ kodu için çağrılar için hem bir üye görebilirsiniz:

![Visual Studio'da C++ kodu için çağrı hiyerarşisi](media/call-hierarchy-cpp.png)

İçin C# ve Visual Basic kodu üyesi çağrıları, ancak gelen çağrıları görebilirsiniz:

![Çağrı hiyerarşisi için C# Visual Studio'daki kod](media/call-hierarchy-csharp.png)

- Genişletirseniz **çağrıları için** düğüm, tüm üyeleri seçilen üyenin çağrı görüntülenir.

- C++, f, genişletmek için **gelen çağrıları** düğümü, seçilen üye tarafından çağrılan tüm üyeleri görüntülenir.

Ardından görmek için arama üyelerin genişletin, **çağrıları için**ve C++ için **gelen çağrıları** düğümleri. Bu, çağıranlar, yığına gitmek aşağıdaki görüntüde gösterildiği gibi sağlar:

![Çağrı hiyerarşisi penceresi genişletilmiş birden çok düzeyine sahip](media/call-hierarchy-csharp-expanded.png)

Sanal veya soyut olarak tanımlanan üyeler için bir **geçersiz kılmaları yöntem adı** düğümü görüntülenir. Arabirim üyeleri için bir **uygulayan yöntem adı** düğümü görüntülenir. Bu Genişletilebilir düğümler aynı seviyede görünür **çağrıları için** ve **gelen çağrıları** düğümleri.

**Arama kapsamı** araç çubuğundaki seçenekleri içeren **My çözüm**, **geçerli proje**, ve **geçerli belge**.

Bir alt üye seçtiğinizde **çağrı hiyerarşisi** ağaç görünümü bölmesinde:

- **Çağrı hiyerarşisi** Ayrıntılar bölmesinde, tüm alt üyenin üst üyesi çağrıldığında kod satırlarını görüntüler.

- **Kod tanımı** penceresi açıksa, görüntüler kod seçilen üyenin (yalnızca C++). Bu pencere hakkında daha fazla bilgi için bkz. [kod yapısını görüntüleme](../../ide/viewing-the-structure-of-code.md).

> [!NOTE]
> **Çağrı hiyerarşisi** özellik bulamazsa yöntem grubu başvuruları burada bir yöntem bir olay işleyicisi eklenir veya bir temsilciye atanmış basamak içerir. Bir yöntem için tüm başvuruları Bul için kullanabileceğiniz **tüm başvuruları Bul** komutu.

## <a name="shortcut-menu-items"></a>Kısayol menü öğesi

Aşağıdaki tabloda, bir düğüm ağaç görünümü bölmesinde sağ tıklattığınızda, kullanılabilen birkaç kısayol menü seçenekleri açıklanmaktadır.

|Bağlam menüsü öğesi|Açıklama|
| - |-----------------|
|**Yeni kök olarak Ekle**|Seçili düğüm için ağaç görünümü bölmesinde yeni bir kök düğümü ekler. Bu belirli bir alt ağaçta ilgilenmeniz odaklanmanızı sağlar.|
|**Kökü Kaldır**|Ağaç görünümü bölmesinde seçilen kök düğümü kaldırır. Bu seçenek, yalnızca bir kök düğümü kullanılabilir.<br /><br /> Ayrıca **kaldırmak kök** araç çubuğu düğmesi seçili kök düğümü kaldırmak için.|
|**Tanıma Git**|Seçili düğümde Tanıma Git komutu çalıştırır. Bu, bir üye çağrısı için orijinal tanımını veya değişken tanımını gider.<br /><br /> Tanıma Git komutu çalıştırmak için Seçili düğüme çift tıklayın veya seçili düğümde F12 tuşuna basın.|
|**Tüm başvuruları Bul**|Seçili düğümde tüm başvuruları Bul komutu çalıştırır. Bu kod satırlarını projenize bu başvuruyu bir sınıf veya üye bulur.<br /><br /> Seçili düğümde tüm başvuruları Bul komutu çalıştırmak için SHIFT + F12 de kullanabilirsiniz.|
|**Kopyala**|Seçili düğümü (ancak alt düğümlerini) içeriğini kopyalar.|
|**Yenileme**|Böylece geçerli bilgilerini görüntüler yeniden genişleterek seçili düğümü daraltır.|