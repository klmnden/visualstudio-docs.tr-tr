---
title: 'Öğretici: Entity Framework ve Visual Studio 2019 ile ASP.NET Core web uygulaması oluşturma'
titleSuffix: ''
description: ASP.NET Core web uygulaması oluşturmadan önce ilk adım olarak, Visual Studio 2019 bu videosu ve adım adım yönergeleri ile nasıl yükleneceğini öğrenin.
ms.custom: get-started
ms.date: 03/31/2019
ms.technology: vs-ide-general
ms.prod: visual-studio-windows
monikerRange: vs-2019
ms.topic: tutorial
ms.devlang: CSharp
author: ardalis
ms.author: tglee
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- aspnet
- dotnetcore
ms.openlocfilehash: 0055c82812c94d3a29cc4f1b949f6b2c62a4445c
ms.sourcegitcommit: 509fc3a324b7748f96a072d0023572f8a645bffc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58859117"
---
# <a name="tutorial-create-your-first-aspnet-core-app-using-entity-framework-with-visual-studio-2019"></a>Öğretici: Visual Studio 2019 ile Entity Framework kullanarak ilk ASP.NET Core uygulamanızı oluşturma

Bu öğreticide, verileri kullanan ASP.NET Core web uygulaması oluşturacak ve Azure'a dağıtın. Bu öğreticide, aşağıdaki adımlardan oluşur:

- [1. Adım: Visual Studio 2019 yükleyin](#step-1-install-visual-studio-2019)
- [2. Adım: İlk ASP.NET Core web uygulamanızı oluşturma](tutorial-aspnet-core-ef-step-02.md)
- [3. Adım: Entity Framework kullanarak verileri ile çalışma](tutorial-aspnet-core-ef-step-03.md)
- [4. Adım: ASP.NET Core uygulamanızı bir Web API'SİNİN kullanıma sunma](tutorial-aspnet-core-ef-step-04.md)
- [5. Adım: ASP.NET Core uygulamanızı Azure'a dağıtma](tutorial-aspnet-core-ef-step-05.md)

## <a name="step-1-install-visual-studio-2019"></a>1. Adım: Visual Studio 2019 yükleyin

Bu video öğreticide ve adım adım yönergeleri ile Visual Studio 2019 yüklemeyi öğrenin. Zaten Visual Studio yüklü değilse, atlayın [2. adım: İlk ASP.NET Core web uygulamanızı oluşturma](tutorial-aspnet-core-ef-step-02.md).

_Bu video ve bunların Visual Studio'yu yükleyin ve ilk ASP.NET Core uygulamanızı oluşturmak için izleme izleyin._

> [!VIDEO https://www.youtube.com/embed/Fz_HAqQGLtY]

## <a name="download-the-installer"></a>Yükleyiciyi indirin

Git [visualstudio.com](https://visualstudio.com) yükleyicisi bulunamadı. Visual Studio 2019 bağlantıyı bulun ve yüklemeyi başlatmak için tıklatın. Visual Studio'nun Ücretsiz bir sürümü Visual Studio Community seçin.

## <a name="start-the-installer"></a>Yükleyiciyi başlatın

İndirme tamamlandıktan sonra tıklayın **çalıştırma** yükleyiciyi başlatmak için.

![Visual Studio 2019 yükleyicisi](media/vs-2019/vs2019-installer.png)

## <a name="choose-workloads"></a>İş yükleri seçin

Visual Studio, birçok farklı türde geliştirme için kullanılabilir ve iş yükleri için derlemek istediğiniz uygulamaları türü için ihtiyacınız olan her şey indirmek kolaylaştırır. Seçin **ASP.NET ve Web geliştirme** ve **.NET Core çoklu platform geliştirme** iş yükleri için şimdi. Her zaman ek iş yüklerinin ve bileşenlerin daha sonra yüklemek için yükleyici denemesine.

![Visual Studio 2019 iş yükleri seçin](media/vs-2019/vs2019-choose-workloads.png)

## <a name="install"></a>Yükleme

Tıklayın **yükleme** ve Visual Studio yükleyip yükleyici sağlar.

## <a name="run-visual-studio-for-the-first-time"></a>Visual Studio'yu ilk kez çalıştırın.

Yükleyici tamamlandığında Visual Studio otomatik olarak başlatma. Oturum açmaya sahip olduğu daha sonra bunu seçtiğiniz artık onunla ancak için ilişkili bazı kullanışlı özellikler istenebilir. Sonraki teması ve geliştirme ayarlarınızı seçin. Bu seçimleri yaptıktan sonra ilk projenizi başlamaya hazır olacaksınız. Tıklayın **yeni bir proje oluşturma** seçip **ASP.NET Core Web uygulaması**.

![Visual Studio 2019 yeni ASP.NET Core Web uygulaması projesi oluşturma](media/vs-2019/vs2019-create-new-project.png)

## <a name="explore-aspnet-core-project-types"></a>ASP.NET Core proje türlerini keşfedin

Proje adı ve konumu seçin, ardından çekme **Oluştur**. Şimdi, ASP.NET Core uygulamanız için kullanılacak şablonu seçin. Aşağıdaki seçeneklerden birini seçebilirsiniz:

- Boş. Sıfırdan başlayın sağlayan boş bir proje şablonu.
- API. Web API'leri için idealdir.
- Web uygulaması. Razor sayfaları ile oluşturulan standart ASP.NET Core web uygulaması.
- Web uygulaması (Model-View-Controller). Model-View-Controller desenini kullanarak, standart ASP.NET Core web uygulaması.
- Angular.
- React.js.
- React.js / Redux.
- Razor sınıf kitaplığı. Razor varlıklar projeler arasında paylaşmak için kullanılır.

Çoğu proje şablonları için de bir kutuyu işaretleyerek Docker desteğini etkinleştirmek seçebileceğiniz olduğunu unutmayın. Değişiklik kimlik doğrulaması düğmesine tıklayarak, kimlik doğrulama desteği de ekleyebilirsiniz. Buradan arasından seçim yapabilirsiniz:

- Kimlik doğrulaması yok.
- Bireysel kullanıcı hesapları. Bu, yerel veya Azure tabanlı bir veritabanında depolanır.
- İş veya Okul hesapları. Bu seçenek, Active Directory, Azure AD kullanır veya Office 365 kimlik doğrulaması için.
- Windows kimlik doğrulaması. İntranet uygulamaları için uygundur.

Kimlik doğrulaması yok ile'standart Web uygulaması şablonu seçin ve tıklayın **Tamam**.

![Visual Studio 2019 ASP.NET Core proje seçenekleri seçin](media/vs-2019/vs2019-choose-aspnetcore-project.png)

## <a name="next-steps"></a>Sonraki adımlar

Sonraki videoda, ilk ASP.NET Core projenizi hakkında daha fazla bilgi edineceksiniz.

[Öğretici: İlk ASP.NET Core Web uygulamanızı oluşturma](tutorial-aspnet-core-ef-step-02.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Öğretici: Kullanmaya başlama C# ve ASP.NET Core](tutorial-aspnet-core.md) videolu kılavuzda olmadan daha ayrıntılı bir eğitim
