---
title: Çeşitli Dosyalar
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- VS.newfile
- VS.OpenWith
- MiscellaneousFilesProject
helpviewer_keywords:
- solutions, miscellaneous files
- builds [Visual Studio], miscellaneous files
- standalone files
- Solution Explorer, miscellaneous files
- Miscellaneous Files folder
- files [Visual Studio], outside of containers
- files [Visual Studio], Miscellaneous Files folder
ms.assetid: 5b96640b-8efe-48a4-8d0a-1ae3f9587e44
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6ec5b5210c37e6beaa71cecb6894ec5b72d96060
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59655291"
---
# <a name="miscellaneous-files"></a>Çeşitli Dosyalar
Kullanmak istediğiniz [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] bağımsız olarak bir proje veya çözüm dosyaları üzerinde çalışmasına düzenleyiciler. Açık bir çözüm olsa da, açın ve bir çözüm veya proje eklemeden dosyaları değiştirin. Bağımsız olarak kapsayıcılardan çalışmak istediğiniz dosyaları diğer dosyalar çağrılır. Çeşitli dosyalar, çözümler ve projeler için dış, yapılarında dahil değildir ve ile kaynak denetimi altında bir çözüme eklenemez.

 Dosyaları bağımsız olarak bir kapsayıcıdan açma çeşitli nedenlerden dolayı kullanışlıdır. Ancak proje tabanlı bir çözüm geliştirmek için çözümün geliştirme integral olmamasına karşın görüntülemek istediğiniz bir dosya olabilir. Geliştirme notları veya yönergeleri, veritabanı şemasını ve kod klipleri ortak örnek verilebilir. Ayrıca, tek başına bir dosya oluşturmak isteyebilirsiniz.

 ![Çözüm projeleri](../../ide/reference/media/projects_solutions_misc.gif)

 Klasör Seçenekleri etkinleştirilip etkinleştirilmediğini çeşitli dosyalar klasörüne dosyalar için Çözüm Gezgini görüntüleyebilirsiniz. Seçenekler arasında ayarlanabilir [belgeler, ortam, Seçenekler iletişim kutusu](../../ide/reference/documents-environment-options-dialog-box.md). Çeşitli dosya kapattıktan sonra bir seçenek için de etkinleştirilmediği sürece, herhangi bir belirli çözüm veya proje ile ilişkili değil.

 Diğer dosyalar klasörünü görüntülerseniz, dosyaların bağlantı olarak temsil eder. Bir çözümü açtığınızda bu klasör bir çözümün bir parçası olmasa da, bazı veya tüm çözüm kapatıldığında açıldıkları çeşitli dosyalar, klasör ayarlarını bağlı olarak yeniden açılır.

> [!NOTE]
> Çeşitli dosyalar klasörüne görünmeyen dosyaların bazıları şunlardır: .zip dosyalarını gibi IDE içinden değiştiremezsiniz dosyaları ve .doc dosyaları. IDE, yalnızca bir dış düzenleyici ile değiştirilebilir dosyaları izlemek değildir.

## <a name="commands-available-in-the-ide"></a>IDE içinde kullanılabilir komutları
 Menüleri, araç çubukları ve dosyanın biçimi temel alarak değişiklik içerdikleri komutlar, açın. Örneğin, bir metin dosyasını açtığınızda, metin düzenleyici araç çubuğu görünür ve kendi komutları kullanılabilir. Ardından bir XML şeması dosyasını açın, XML şema araç çubuğu görünür. XML şema kümenizdeki düzenlerken, metin düzenleyici araç çubuğunun komutları (veya araç) kullanılamaz. XML Şeması etkin pencere olup, bu nedenle, geçerli seçim bağlamı içerir. Bir proje dosyası ve çeşitli dosyası arasında geçiş yaptığınızda, projeyle ilgili tüm komutlar kaybolur ve yalnızca çeşitli dosyayı doğrudan ilgili görünür.

## <a name="folder-display-options"></a>Klasör görünen seçenekleri
 Çeşitli klasörü için görüntüleme seçeneklerini ayarlayabilirsiniz, böylece rağmen diğer tüm dosyalar açılmadı klasör görünür. Çözüm dosyası, çeşitli dosyalar listesini kalıcı olarak yönetmez. Bu, dosyaların en son kullanılan kullanıcı başına (MRU) listesini unutmayın sağlayan isteğe bağlı bir özellik kullanır.

## <a name="see-also"></a>Ayrıca Bkz.

- [Çözümler ve Projeler](../../ide/solutions-and-projects-in-visual-studio.md)
- [Belgeler, Ortam, Seçenekler İletişim Kutusu](../../ide/reference/documents-environment-options-dialog-box.md)