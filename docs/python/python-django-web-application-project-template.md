---
title: Python Django web projesi şablonu
description: Python Django framework kullanılarak yazılmış web uygulamaları için Visual Studio şablonları genel bakış.
ms.date: 11/12/2018
ms.prod: visual-studio-dev15
ms.technology: vs-python
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: douge
ms.workload:
- python
- data-science
ms.openlocfilehash: 1e00fd7df429b219589e1e49ddbc5ccadca5e032
ms.sourcegitcommit: 6a955a2d179cd0e137942389f940d9fcbbe125de
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/13/2018
ms.locfileid: "51607438"
---
# <a name="django-web-project-template"></a>Django web projesi şablonu

[Django](https://www.djangoproject.com/) , hızlı, güvenli ve ölçeklenebilir bir web geliştirme için tasarlanan yüksek düzeyli bir Python altyapısıdır. Visual Studio'da Python desteği, yapıyı bir Django tabanlı bir web uygulamasının ayarlamak için birçok proje şablonları sağlar. Visual Studio'da bir şablon kullanmak için **dosya** > **yeni** > **proje**"Django" için arama yapın ve listeden  **Django Web projesi boş**, **Django Web projesi**, ve **yoklamalar Django Web projesi** şablonları. Bkz: [öğrenin Django öğretici](learn-django-in-visual-studio-step-01-project-and-solution.md) tüm şablonları kılavuz.

Visual Studio, Django projeleri için IntelliSense sağlar:

- Bağlam değişkenleri şablona geçirildi:

    ![Bağlam değişkenleri için IntelliSense](media/template-django-intellisense.png)

- Etiketleme ve için hem yerleşik olanları filtreleme ve kullanıcı tanımlı:

    ![Etiketleri ve filtreler için IntelliSense](media/template-django-intellisense-filter.png)

- Sözdizimi: Katıştırılmış CSS ve JavaScript için renklendirme

    ![CSS IntelliSense](media/template-django-intellisense-css.png)

    ![JavaScript IntelliSense](media/template-django-intellisense-js.png)

Visual Studio ayrıca sağlar tam [hata ayıklama desteği](debugging-python-in-visual-studio.md) Django projeleri için: 

![Kesme noktaları](media/template-django-debugging.png)

Django projelerin aracılığıyla yönetilen tipik kendi *manage.py* dosyasını Visual Studio izlediği varsayılır. Giriş noktası olarak bu dosyayı kullanarak durdurursanız, proje dosyası temelde bölün. Bu durumda için ihtiyacınız [projeden varolan dosyaları yeniden](managing-python-projects-in-visual-studio.md#create-a-project-from-existing-files) olmadan bir Django projesi olarak işaretleniyor.

## <a name="django-management-console"></a>Django Yönetim Konsolu

Django Yönetim Konsolu çeşitli komutlara üzerinden erişilen **proje** menüsü veya projeye sağ tıklayarak **Çözüm Gezgini**.

- **Django Kabuğu'nu açın**: uygulama Bağlamınızı Modellerinizi yönetmenize olanak sağlayan bir kabuk açılır:

    ![Konsol](media/template-django-console-shell.png)

- **Django eşitleme DB**: yürütür `manage.py syncdb` içinde bir **etkileşimli** penceresi:

    ![Konsol](media/template-django-console-sync-db.png)

- **Statik toplamak**: yürütür `manage.py collectstatic --noinput` tarafından belirtilen yol için tüm statik dosyaları kopyalamak için `STATIC_ROOT` içinde *settings.py*.

    ![Konsol](media/template-django-console-collect-static.png)

- **Doğrulama**: yürütür `manage.py validate`, hangi raporların tarafından belirtilen yüklü modellerindeki herhangi bir doğrulama hatası `INSTALLED_APPS` içinde *settings.py*:

    ![Konsol](media/template-django-console-validate.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Django öğretici öğrenin](learn-django-in-visual-studio-step-01-project-and-solution.md)
- [Azure App Service’e yayımlama](publishing-python-web-applications-to-azure-from-visual-studio.md)
