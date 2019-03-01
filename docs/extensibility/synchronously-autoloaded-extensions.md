---
title: Zaman uyumlu bir şekilde otomatik yüklenen uzantılar
ms.date: 02/16/2019
ms.topic: conceptual
ms.assetid: 822e3cf8-f723-4ff1-8467-e0fb42358a1f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ad3831fb06d23f622f85a55f5efd0a5650ca5e47
ms.sourcegitcommit: 62149c96de0811415e99bb1e0194e76c320e1a1e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/28/2019
ms.locfileid: "57007169"
---
# <a name="synchronously-autoloaded-extensions"></a>Zaman uyumlu bir şekilde otomatik yüklenen uzantılar

Zaman uyumlu olarak autoloaded uzantılar Visual Studio performansını olumsuz bir etkiye sahip ve zaman uyumsuz sorsorgu yerine kullanacak şekilde dönüştürülmeleri. Uzantı, zaman uyumlu olarak autoloaded yüklenirken Visual Studio 2019 Önizleme 2'de başlayarak, kullanıcılar bilgilendirildi. Uzantı yükleme ve normal şekilde çalışır.

![Uzantı uyumluluk Uyarısı](media/extension-compatibility-warning.png)

Kullanıcılar şunları yapabilir:

- Tıklayarak **daha fazla bilgi edinin** bu bilgileri sayfasına ulaşmak için.

- Tıklayarak **performansı yönetme** açmak için [Performans Yöneticisi iletişim kutusu](#performance-manager-dialog) uzantıları ve araç pencerelerini ile performans sorunlarını gösterir.

- Tıklayarak **bu iletiyi tekrar gösterme** bildirimi kapatmak için. Bu seçeneğin belirlenmesi, zaman uyumlu olarak autoloaded uzantılardan gelecekteki tüm bildirimleri engeller. Kullanıcılar, diğer Visual Studio özellikleri hakkında bildirim almaya devam edebilir.

### <a name="performance-manager-dialog"></a>Performans Yöneticisi iletişim kutusu

![Performans Yöneticisi iletişim kutusu](media/performance-manager.png)

Görünür zaman uyumlu olarak herhangi bir paket içinde herhangi bir kullanıcı oturumlarını yüklenen tüm uzantıları **API'leri kullanım dışı** sekmesi.

* Kullanıcılar tıklayabilirsiniz **Bu sorun hakkında daha fazla bilgi** kaldırılmış API'ler hakkında daha fazla bilgi toplayın.
* Kullanıcılar kendi uzantı satıcıları geçiş ilerleme durumu iletişim kurabilirsiniz.

Uzantı yazarları geçirilmesine yönelik yönergeler bulabilir zaman uyumsuz sorsorgu paketlere [AsyncPackage geçiş](https://github.com/Microsoft/VSSDK-Extensibility-Samples/tree/master/AsyncPackageMigration).
