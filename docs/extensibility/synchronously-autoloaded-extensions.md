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
ms.openlocfilehash: d23a19ad42f665f471274ee75f328056dd55b17d
ms.sourcegitcommit: cd21b38eefdea2cdefb53e68e7a30b868e78dd6b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2019
ms.locfileid: "66037095"
---
# <a name="synchronously-autoloaded-extensions"></a>Zaman uyumlu bir şekilde otomatik yüklenen uzantılar

Zaman uyumlu olarak autoloaded uzantılar Visual Studio performansını olumsuz bir etkiye sahip ve zaman uyumsuz sorsorgu yerine kullanacak şekilde dönüştürülmeleri. Uzantı, zaman uyumlu olarak autoloaded yüklenirken Visual Studio 2019 Önizleme 2'de başlayarak, kullanıcılar bilgilendirildi. Uzantı yükleme ve normal şekilde çalışır.

![Uzantı uyumluluk Uyarısı](media/extension-compatibility-warning.png)

Kullanıcılar şunları yapabilir:

- Tıklayarak **daha fazla bilgi edinin** bu bilgileri sayfasına ulaşmak için.

- Tıklayarak **performansı yönetme** açmak için [Performans Yöneticisi iletişim kutusu](#performance-manager-dialog) uzantıları ve araç pencerelerini ile performans sorunlarını gösterir.

- Tıklayarak **bu iletiyi tekrar gösterme** bildirimi kapatmak için. Bu seçeneğin belirlenmesi, zaman uyumlu olarak autoloaded uzantılardan gelecekteki tüm bildirimleri engeller. Kullanıcılar, diğer Visual Studio özellikleri hakkında bildirim almaya devam edebilir.

## <a name="performance-manager-dialog"></a>Performans Yöneticisi iletişim kutusu

![Performans Yöneticisi iletişim kutusu](media/performance-manager.png)

Görünür zaman uyumlu olarak herhangi bir paket içinde herhangi bir kullanıcı oturumlarını yüklenen tüm uzantıları **API'leri kullanım dışı** sekmesi.

* Kullanıcılar tıklayabilirsiniz **Bu sorun hakkında daha fazla bilgi** kaldırılmış API'ler hakkında daha fazla bilgi toplayın.
* Kullanıcılar kendi uzantı satıcıları geçiş ilerleme durumu iletişim kurabilirsiniz.

Uzantı yazarları geçirilmesine yönelik yönergeler bulabilir zaman uyumsuz sorsorgu paketlere [AsyncPackage geçiş](https://github.com/Microsoft/VSSDK-Extensibility-Samples/tree/master/AsyncPackageMigration).

## <a name="specify-synchronous-autoload-settings-using-group-policy"></a>Grup İlkesi kullanarak zaman uyumlu otomatik yükleme ayarlarını belirtin

Visual Studio 2019 güncelleştirme 1, varsayılan olarak, Visual Studio yükleme blokları zaman uyumlu sorsorgu başlatılıyor. Grup İlkesi'ni etkinleştirdiğinizde, Visual Studio tek tek bilgisayarlarda zaman uyumlu sorsorgu izin verecek şekilde yapılandırabilirsiniz. Bunu yapmak için aşağıdaki anahtarı kayıt defteri tabanlı bir ilke ayarlayın:

**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\VisualStudio\SynchronousAutoload**

Giriş = **izin**

Değer (DWORD) =
* **0** zaman uyumlu sorsorgu izin verilmiyor
* **1** zaman uyumlu sorsorgu izin verilir

Visual Studio 2019 güncelleştirme 1'deki eşzamanlı otomatik yükleme ayarları hakkında daha fazla bilgi için bkz. [eşzamanlı Sorsorgu davranış](https://aka.ms/AA52xzw) sayfası.
