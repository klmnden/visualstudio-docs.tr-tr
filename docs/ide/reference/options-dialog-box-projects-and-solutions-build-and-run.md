---
title: Seçenekler İletişim Kutusu, Projeler ve Çözümler, Derleme ve Çalıştırma
ms.date: 07/14/2017
ms.technology: vs-ide-compile
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Projects.Build_and_Run
helpviewer_keywords:
- builds [Visual Studio], setting up
- run actions
- debugger, run options
ms.assetid: c884976e-c0df-4c6d-8e3a-856ea2bd547c
author: ghogen
ms.author: ghogen
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 24ba5bbf34ecc12c2508c538e74909ee0a10aef4
ms.sourcegitcommit: 85d66dc9fea3fa49018263064876b15aeb6f9584
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/24/2019
ms.locfileid: "68461386"
---
# <a name="options-dialog-box-projects-and-solutions--build-and-run"></a>Seçenekler iletişim kutusu: Projeler ve çözümler \> derleme ve çalıştırma

Bu iletişim kutusunda, aynı anda oluşturulabilecek en fazla C++ C# proje sayısını, belirli varsayılan derleme davranışlarını ve bazı derleme günlüğü ayarlarını belirtebilirsiniz. Bu seçeneklere erişmek için **Araçlar** > **Seçenekler** sırasıyla **Projeler ve çözümler**' i seçin ve ardından **Oluştur ve Çalıştır**' ı seçin.

**En fazla paralel proje derlemesi sayısı**

Aynı anda oluşturulabilecek maksimum C++ ve C# proje sayısını belirtir. Yapı işlemini iyileştirmek için, en fazla paralel proje derleme sayısı, bilgisayarınızın CPU sayısına otomatik olarak ayarlanır. Maksimum değer 32 ' dir.

**Çalıştırma sırasında yalnızca başlangıç projelerini ve bağımlılıklarını oluşturun**

**F5** tuşunu, **hata** > **ayıklamayı Başlat** menü komutunu veya **Yapı** menüsünde uygulanabilir komutları kullandığınızda yalnızca başlangıç projesini ve bağımlılıklarını oluşturur. İşaretlenmezse, tüm projeler ve bağımlılıklar oluşturulur.

**Çalıştırıldığında, projeler güncel olmadığında**

*Yalnızca projeler C++ için geçerlidir.*

**F5** veya **Debug** > **Start hata ayıklama** komutuyla bir proje çalıştırırken, bir proje yapılandırması güncel değilse **derlemek için** varsayılan ayar isteminde bir ileti görüntülenir. Her çalıştırılışında projeyi derlemek için **her zaman oluştur** ' u seçin. Bir proje çalıştırıldığında tüm otomatik yapıları gizlemek için **hiçbir zaman derlemeyi** seçin.

**Çalıştırıldığında, derleme veya dağıtım hataları oluştuğunda**

*Yalnızca projeler C++ için geçerlidir.*

**F5** veya **Debug** > **Start hata ayıklama** komutuyla bir proje çalıştırırken, **başlatılacak** varsayılan ayar, derleme başarısız olsa bile bir projenin çalıştırılması gerekiyorsa bir ileti görüntüler. Son iyi derlemeyi otomatik olarak başlatmak için **eski sürümü Başlat** ' ı seçin. Bu, çalışan kod ve kaynak kodu arasındaki uyuşmazlıkları ortaya çıkmasına neden olabilir. İletiyi bastırmak için **başlatma** ' yı seçin.

**Yeni çözümler için, seçili olan projeyi başlangıç projesi olarak kullanın**

Bu seçenek ayarlandığında, yeni çözümler seçili olan projeyi başlangıç projesi olarak kullanır.

**MSBuild proje derlemesi çıkış ayrıntı düzeyi**

**Çıkış** penceresinde yapı işlemindeki bilgilerin ne kadar görüntülendiğini belirler.

**MSBuild proje derleme günlük dosyası ayrıntı düzeyi**

*Yalnızca projeler C++ için geçerlidir.*

*\\ProjectName > \debug \<ProjectName>.\<log konumunda bulunan yapı günlüğü dosyasına ne kadar bilgi yazıldığını belirler.\\*

## <a name="see-also"></a>Ayrıca bkz.

- [Derleme ve Oluşturma](../../ide/compiling-and-building-in-visual-studio.md)
- [Seçenekler Iletişim kutusu, projeler ve çözümler](projects-and-solutions-options-dialog-box.md)
- [Seçenekler İletişim Kutusu, Projeler ve Çözümler, Web Projeleri](options-dialog-box-projects-and-solutions-web-projects.md)