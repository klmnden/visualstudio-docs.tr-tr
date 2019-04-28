---
title: Seçenekler İletişim Kutusu, Projeler ve Çözümler, Derleme ve Çalıştırma
ms.date: 07/14/2017
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Projects.Build_and_Run
helpviewer_keywords:
- builds [Visual Studio], setting up
- run actions
- debugger, run options
ms.assetid: c884976e-c0df-4c6d-8e3a-856ea2bd547c
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3d0f24dc1afa875183f03e15e46cc2331f27cbf0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62996830"
---
# <a name="options-dialog-box-projects-and-solutions--build-and-run"></a>Seçenekler iletişim kutusu: Projeler ve çözümler \> derleme ve çalıştırma

Bu iletişim kutusunda, C++ üst sınırını belirtebilirsiniz veya C# aynı anda oluşturabilirsiniz projeleri, belirli bir varsayılan derleme davranışları ve bazı günlük ayarlarını oluşturun. Bu seçeneklere erişmek için seçin **Araçları** > **seçenekleri** genişletin **projeler ve çözümler**ve ardından **derleme ve çalıştırma**.

**derleme en fazla paralel proje sayısı**

C++ üst sınırını belirtir ve C# projeleri aynı anda oluşturabilirsiniz. Derleme işlemi iyileştirmek için en fazla paralel proje yapılandırma sayısını bilgisayarınızın CPU sayısını otomatik olarak ayarlanır. En fazla 32'dir.

**Başlangıç projelerini ve bağımlılıkları sadece çalıştırıldığında Derle**

Kullandığınızda, yalnızca başlangıç projesi ve bağımlılıklarını yapılar **F5** anahtar **hata ayıklama** > **hata ayıklamayı Başlat** menü komutu ya da geçerli komutları **derleme** menüsü. İşaretli değilse, tüm projelerinizi ve bağımlılıklarınızı oluşturulur.

**Çalıştırmada, projelerin güncel olduğunda**

*Yalnızca C++ projeleri için geçerlidir.*

Projeyle çalışırken **F5** veya **hata ayıklama** > **hata ayıklamayı Başlat** komut, varsayılan ayar **oluşturmak komut istemi** bir proje yapılandırması eski ise bir ileti görüntüler. Seçin **her zaman derleme** her çalıştırıldığında, projeyi oluşturmak için. Seçin **asla derleme** bir projeyi çalıştırdığınızda, tüm otomatik derlemeler bastırmak için.

**Alıştırmada, ne zaman derleme veya dağıtım hataları oluşuyor**

*Yalnızca C++ projeleri için geçerlidir.*

Projeyle çalışırken **F5** veya **hata ayıklama** > **hata ayıklamayı Başlat** komut, varsayılan ayar **başlatmakkomutistemi**bir proje, derleme başarısız olsa bile çalıştırılması gereken bir ileti görüntüler. Seçin **başlatma eski sürümü** çalışan kodu ve kaynak kodu uyuşmazlıklarını sonuçlanabilir son iyi derlemeden otomatik olarak başlatılacak. Seçin **başlatma** iletiyi bastırmak için.

**Yeni çözümleri şu anda seçili projeyi başlangıç projesi olarak kullanın.**

Bu seçenek ayarlandığında, yeni çözümleri şu anda seçili projeyi başlangıç projesi olarak kullanın.

**MSBuild proje oluşturması çıkış ayrıntısı**

Derleme işlemi ne kadar bilgi görüntülenen belirler **çıkış** penceresi.

**MSBuild proje derleme günlük dosyası ayrıntısı**

*Yalnızca C++ projeleri için geçerlidir.*

Şu konumdadır derleme günlüğü dosyası için ne kadar bilgi yazılacağını belirler  *\\ \<ProjectName > \Debug\\\<ProjectName > .log*.

## <a name="see-also"></a>Ayrıca bkz.

- [Derleme ve Oluşturma](../../ide/compiling-and-building-in-visual-studio.md)
- [Seçenekler iletişim kutusu, projeler ve çözümler](projects-and-solutions-options-dialog-box.md)
- [Seçenekler İletişim Kutusu, Projeler ve Çözümler, Web Projeleri](options-dialog-box-projects-and-solutions-web-projects.md)