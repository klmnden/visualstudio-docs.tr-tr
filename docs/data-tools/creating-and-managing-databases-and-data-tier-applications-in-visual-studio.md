---
title: Veritabanı projeleri, sunucu projeleri ve Visual Studio projelerinde DAC
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- managing change, databases
- database features of Visual Studio, managing change
- databases, managing change
- managing change, database servers
ms.assetid: 40b51f5a-d52c-44ac-8f84-037a0917af33
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-data-tools
ms.workload:
- data-storage
ms.openlocfilehash: 7f3d3f8dc34cf354fd6cb6b6689701dab791132d
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49942536"
---
# <a name="database-projects-and-data-tier-applications-in-visual-studio"></a>Veritabanı projeleri ve Visual Studio'daki veri katmanı uygulamaları

Veritabanı projeleri yeni veritabanları oluşturmak için kullanabileceğiniz yeni veri katmanı uygulamaları (Dac'ler) ve var olan veritabanlarını ve veri katmanı uygulamaları güncelleştirmek için. Hem veritabanı projeleri hem de DAC projeleri çok yönetilen veya yerel kod için bu teknikler uyguladığınız aynı şekilde, veritabanı geliştirme çalışmalarınızda kullanmanız için sürüm denetimi ve proje yönetimi teknikleri uygulanmasını sağlar. DAC proje, veritabanı projesi veya bir sunucu projesi oluşturma ve sürüm denetimi altında koyarak veritabanları ve veritabanı sunucuları değişiklikleri yönetme geliştirme ekibinize yardımcı olabilir. Ekip üyelerinin olun, derleme ve değişiklikleri bir yalıtılmış bir geliştirme ortamı veya korumalı alan, takım paylaşmadan önce test dosyaları kontrol edebilirsiniz. Kod kalitesinin sağlanmasına yardımcı olmak için takımınızın tamamlayın ve değişiklikleri üretime dağıtmadan önce tüm değişiklikleri veritabanını belirli bir sürümü için bir hazırlama ortamında test.

Veri katmanı uygulamaları tarafından desteklenen veritabanı özelliklerin bir listesi için bkz. [veri katmanı uygulamalarında desteklenen özellikleri](/previous-versions/visualstudio/visual-studio-2010/ee362013(v=vs.100)). Veri katmanı uygulamaları tarafından desteklenmeyen özellikleri veritabanınızdaki kullanırsanız, veritabanınıza değişiklikleri yönetmek için bunun yerine bir veritabanı projesi kullanmanız gerekir.

## <a name="common-high-level-tasks"></a>Ortak bir üst düzey görevler

| Üst düzey görev | Destekleyici İçerik |
| - | - |
| **Veri katmanı uygulaması geliştirmeye başla:** A DAC ile sunulan yeni bir kavram olan [!INCLUDE[sskatmai_r2](../data-tools/includes/sskatmai_r2_md.md)] tanımını içeren bir [!INCLUDE[ssNoVersion](../data-tools/includes/ssnoversion_md.md)] veritabanını ve destekleyen bir istemci-sunucu veya 3 katmanlı tarafından kullanılan nesneleri örneği uygulama. Bir DAC, tablolar ve görünümler, oturum açma bilgileri gibi örnek varlıkları birlikte gibi nesneleri içerir. Visual Studio DAC proje oluşturma, DAC paket dosyası derleme ve dağıtım örneği için bir veritabanı yöneticisi, DAC paket dosyası göndermek için kullanabileceğiniz [!INCLUDE[ssNoVersion](../data-tools/includes/ssnoversion_md.md)] veritabanı altyapısı. | -   [Oluşturma ve veri katmanı uygulamaları yönetme](http://go.microsoft.com/fwlink/?LinkId=160741)<br />-   [SQL Server Management Studio](http://go.microsoft.com/fwlink/?LinkId=227328) |
| **Yinelemeli veritabanı geliştirme gerçekleştirme:** bir geliştirici veya test edici ise, proje bölümlerini denetleyin ve ardından bunları bir yalıtılmış geliştirme ortamında güncelleştirin. Bu ortam türünü kullanarak, diğer takım üyeleri etkilemeden değişikliklerinizi test edebilirsiniz. Değişiklik tamamlandıktan sonra burada diğer takım üyelerinin yaptığınız değişiklikleri alabilir ve yapı ve bunları bir test sunucusuna dağıtmak geri sürüm denetimine, dosyaları denetleyin. | -   [Sorgu ve metin düzenleyiciler (SQL Server Management Studio)](http://go.microsoft.com/fwlink/?LinkId=227327)<br />-   [Transact-SQL hata ayıklayıcısı](http://go.microsoft.com/fwlink/?LinkId=227324) |
| **Doğrulama prototip oluşturma, test sonuçları ve değiştirme veritabanı betikleri ve nesneleri:** kullanabileceğiniz [!INCLUDE[tsql](../data-tools/includes/tsql_md.md)] herhangi biri şu genel görevleri gerçekleştirmek için düzenleyici. | -   [Sorgu ve metin düzenleyiciler (SQL Server Management Studio)](http://go.microsoft.com/fwlink/?LinkId=227327) |

## <a name="see-also"></a>Ayrıca bkz.

- [.NET için Visual Studio veri araçları](../data-tools/visual-studio-data-tools-for-dotnet.md)
