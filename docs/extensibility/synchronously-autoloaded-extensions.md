---
title: Zaman uyumlu olarak autoloaded uzantıları
ms.date: 02/16/2019
ms.topic: conceptual
ms.assetid: 822e3cf8-f723-4ff1-8467-e0fb42358a1f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 960fd54564bc25a8338461c30cd8a893e277b5a5
ms.sourcegitcommit: 23feea519c47e77b5685fec86c4bbd00d22054e3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56844610"
---
# <a name="synchronously-autoloaded-extensions"></a>Zaman uyumlu olarak autoloaded uzantıları

Zaman uyumlu olarak autoloaded uzantılar Visual Studio performansını olumsuz bir etkiye sahip ve zaman uyumsuz sorsorgu yerine kullanacak şekilde dönüştürülmeleri. Visual Studio 2019 Önizleme 2'de başlayarak, uzantı autoloaded zaman uyumlu olarak yüklenirken kullanıcı bildirilir. Uzantı yükleme ve normal şekilde çalışır.

![Uzantı uyumluluk Uyarısı](media/extension-compatibility-warning.png)

1. Kullanıcılar tıklayabilirsiniz **daha fazla bilgi edinin** bu bilgileri sayfasına ulaşmak için.

3. Kullanıcılar tıklayabilirsiniz **performansı yönetme** açmak için [Performans Yöneticisi iletişim kutusu](#performance-manager-dialog) uzantıları ve araç pencerelerini ile performans sorunlarını gösterir.

3. Kullanıcılar tıklayabilirsiniz **bu iletiyi tekrar gösterme** bildirimi kapatmak için. Bu seçeneğin belirlenmesi, zaman uyumlu olarak autoloaded uzantılardan tüm gelecekteki bildirimleri de engeller. Kullanıcılar, diğer Visual Studio özellikleri hakkında bildirim almaya devam edebilir.

### <a name="performance-manager-dialog"></a>Performans Yöneticisi iletişim kutusu

  ![Performans Yöneticisi iletişim kutusu](media/performance-manager.png)

Zaman uyumlu olarak herhangi bir paket içinde herhangi bir kullanıcı oturumlarını yüklenen tüm uzantıları görünecek **API'leri kullanım dışı** sekmesi.

* Kullanıcılar tıklayabilirsiniz **Bu sorun hakkında daha fazla bilgi** kaldırılmış API'ler hakkında daha fazla bilgi toplayın.
* Kullanıcılar kendi uzantı satıcıları geçiş ilerleme durumu iletişim kurabilirsiniz.

Uzantı yazarları geçirilmesine yönelik yönergeler bulabilir zaman uyumsuz sorsorgu paketlere [AsyncPackage geçiş](https://github.com/Microsoft/VSSDK-Extensibility-Samples/tree/master/AsyncPackageMigration).
