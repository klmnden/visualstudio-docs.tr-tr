---
title: Visual Studio hata ayıklayıcısı sözlüğü | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- glossary [Debugging SDK]
- debugging [Debugging SDK], glossary
ms.assetid: 4a2cfaab-1fbd-4a23-bd00-9ac4cc50d7fd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 36c6ea7d4559d63f8d230d73e0df5f14fc21a0b5
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65458032"
---
# <a name="visual-studio-debugger-glossary"></a>Visual Studio Hata Ayıklayıcısı Sözlüğü
İçinde kullanılan terimleri şunlardır [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] hata ayıklama SDK'sı.

## <a name="terms"></a>Koşulları
 kod içinde bir kesme noktası için bir soyutlamayı kesme sınırı. İlişkili bir kesme noktası ve bir kesme noktası yönerge kodu stream'de arasında bire bir ilişki yoktur. Bellekten kod, bağlı kesme noktaları arasındaki bağlamayı.

 nedensellik ilişkilerini birden çok fiziksel iş parçacıkları, işlemler ve makine mantıksal bir yürütme iş parçacığı izlemek ve bu iş parçacığının etkin kalma süresi söz konusu mantıksal iş parçacığının herhangi bir anda çağrı yığınını yeniden olanağı sağlar.

 kod bağlamı, kodda hata ayıklama altyapısı tarafından tanınan bir konumdaki bir Özet sağlar. Çalışma zamanı mimarileri için kod bağlamı bir programın yönerge stream'de bir adrestir. Hangi kod yönergeleri ile gösterilebilir değil nontraditional diller için kod bağlamı başka yollarla temsil edilebilir.

 kod yolu yürütme burada bir dalın alınması veya bir işlev çağrısı yapıldığında kodda bir noktayı temsil eder. Bir yığın izlemesi temelde işlevi çağrısı kod yolları bir listesidir.

 bir çalışma zamanı mimarisini hata ayıklamasına izin hata ayıklama altyapısı (DE) bir bileşen. Hata ayıklama altyapısı yorumlayıcı veya işletim sistemi ile birlikte çalışır ve yürütme denetimi, kesme noktaları ve ifade değerlendirme gibi hata ayıklama hizmetleri sağlar.

 Belge bağlamı, hata ayıklama altyapısı tarafından tanınan bir kaynak dosyası belgedeki bir konumdaki bir Özet sağlar. Çoğu dil için bir belge bağlamına kaynak dosyada bir konumdur. Kaynak dosyasını bir metin olmayabilir nontraditional diller için bir belge bağlamı başka bir yolla tarafından temsil edilebilir. Ayrıca bkz: *belge konumu*.

 Belge konumu, IDE bilinen kaynak dosyada bir konumdaki bir Özet sağlar. Çoğu dil için belge konumunu kaynak dosyada bir konumdur. Nontraditional diller için belge konumunu başka şekillerde temsil edilebilir. Ayrıca bkz: *belge bağlamına*.

 hata kesme noktası için bir bekleyen kesme noktasının hata açıklayan bir Özet. Bir hata kesme noktası bekleyen kesme noktasının veya bekleyen kesme noktasının bağlamanın dışında bir kod konuma engelleyen diğer bilgilerle ilişkili ifade bekleyen kesme noktasının konumunu hata açıklayabilir.

 Değerlendirme bağlamı, programlama bir bağlamın ifade değerlendirmesi için bir Özet sağlar. Genellikle, bir değerlendirme bağlamı bir kapsamıdır. Bir ifadenin bağlamında ifade değerlendirme yaparken oluşturma noktasında eşleşen kapsam kuralları ifade bağlamı sağlar. Örneğin, bir yığın çerçevesinde oluşturulan bir ifade bağlamı, yerel değişkenler, yöntem parametreleri, sınıf üyeleri (varsa) ve genel değişkenler değerlendirmesi için bağlamı sağlayacaktır.

 Geçerli yığın çerçevesi bir yerde özel durum işleme mekanizmasını olsa bile, özel durum bir hata ayıklama altyapısı tarafından ele geçirilse bir özel durum kesildi.

 JustMyCode yalnızca bir kullanıcıya ait kodu hata ayıklama ve sistem kodu gibi tüm ara kod yoksayılıyor kavramı — kaynak kodu, sistem kodunu kullanılabilir olsa bile.

 kesme noktası yüklenir ve kesme noktaları sanallaştırmak için yol önce sırasında ve sonrasında kod kesme noktaları için bir Özet sağlar. Bir bekleyen kesme noktası:

- Bir veya daha fazla program kodunda bir kesme noktası bağlamak için gerekli tüm bilgileri içerir.

- Bir veya daha fazla program içinde birden çok kod konumlara bağlayabilirsiniz.

- Hiçbir zaman kendisi koduna bağlar.

  Her zaman kod yükler, bir programdaki tüm bekleyen kesme noktalarını bunlar bağlayabilirsiniz olmadığını görmek için denetlenir. Bir bekleyen kesme noktasının, bağlanan tüm bağımlı kesme noktalarını içerecek şekilde bildirilir.

  fiziksel bir Win32 işlemi işleyin. Bir işlem birden çok programları içerebilir. Ayrıca bkz: *program*.

  belirli bir çalışma zamanı mimarisi içinde çalışan tek bir ad alanında program. Ayrıca bkz: *işlem*.

  oturum hata ayıklama Yöneticisi (SDM) herhangi bir sayıda herhangi bir sayıda makine üzerinde birden çok işlem programlarında hata ayıklama hata ayıklama altyapısı herhangi bir sayıda yönetir. Temel düzeyde, SDM çoğaltıcı hata ayıklama altyapısını ' dir. Ayrıca, SDM IDE hata ayıklama oturumu birleşik bir görünümünü sağlar.

  belirli bir çerçeve olan hesaplamayı durumunu ve belirli düzeyde bir iç içe geçmiş işlev çağrıları, yığın çerçevesini temsil eder.

  Genelleştirilmiş en az bir programda yığın tabanlı yönerge yürütme kavramı iş parçacığı.

  Uyarı kesme noktası açıklayan bir bekleyen kesme noktasının bir uyarı için bir Özet. Bir uyarı kesme noktası neden bekleyen kesme noktası henüz bir kod konuma bağlı olmayan bir nedeni açıklanmaktadır. Bu kodun henüz bekleyen kesme noktasının tarafından açıklanan konumu veya başka bir nedenle yüklememiş emin olabilir.

## <a name="see-also"></a>Ayrıca bkz.
- [Visual Studio Hata Ayıklayıcı Genişletilebilirliği](../../../extensibility/debugger/visual-studio-debugger-extensibility.md)