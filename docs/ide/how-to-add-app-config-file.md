---
title: Bir projeye bir app.config dosyası ekleme
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
dev_langs:
- CSharp
helpviewer_keywords:
- app.config files, adding to C# projects
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 11bc55316414298cf61a27854182f4831feb1ded
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53910106"
---
# <a name="how-to-add-an-application-configuration-file-to-a-c-project"></a>Nasıl Yapılır: Bir uygulama yapılandırma dosyasına ekleyin bir C# proje

Bir uygulama yapılandırma dosyasına ekleyerek (*app.config* dosyası) için bir C# projesi, ortak dil çalışma zamanının nasıl bulur ve derleme dosyalarını yükler özelleştirebilirsiniz. Uygulama yapılandırma dosyaları hakkında daha fazla bilgi için bkz. [çalışma zamanı (.NET Framework) derlemeleri nasıl bulur](/dotnet/framework/deployment/how-the-runtime-locates-assemblies).

> [!NOTE]
> UWP uygulamaları içermeyen bir *app.config* dosya.

Projenizi yapılandırdığınızda, geliştirme ortamı otomatik olarak kopyalar, *app.config* dosya, dosya adı yürütülebilir dosyanızın eşleştirilecek kopyanın değiştirir ve sonra bu kopya taşır **bin** Dizin.

## <a name="to-add-an-application-configuration-file-to-a-c-project"></a>Bir uygulama yapılandırma dosyasına eklemek için bir C# proje

1. Menü çubuğunda, **proje** > **Yeni Öğe Ekle**.

     **Yeni Öğe Ekle** iletişim kutusu görüntülenir.

1. Genişletin **yüklü** > **Visual C# öğeleri**ve ardından **uygulama yapılandırma dosyası** şablonu.

1. İçinde **adı** metin kutusuna bir ad girin ve ardından **Ekle** düğmesi.

     Adlı bir dosya *app.config* projenize eklenir.

## <a name="see-also"></a>Ayrıca bkz.

- [Uygulama ayarlarını yönetme (.NET)](../ide/managing-application-settings-dotnet.md)
- [Yapılandırma dosyası şeması (.NET Framework)](/dotnet/framework/configure-apps/file-schema/index)
- [Uygulamaları (.NET Framework) yapılandırma](/dotnet/framework/configure-apps/index)