---
title: VC++ Proje Ayarları, Projeler ve Çözümler, Seçenekler İletişim Kutusu
ms.date: 08/02/2017
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Projects.VCBuild
helpviewer_keywords:
- builds [Visual Studio], logs
- build process [C++]
- files [Visual Studio], built by C/C++ compiler
- file extensions, built by C or C++ compiler
- cl.exe compiler, file extensions
- extensions, files built by C or C++ compiler
- BuildLog.htm
ms.assetid: 56420efd-6a95-464e-b890-e2b38c48d66a
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: cb53b30b00f6f55bce21fd0069aac733d4a59228
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54938048"
---
# <a name="vc-project-settings-projects-and-solutions-options-dialog-box"></a>VC++ Proje Ayarları, Projeler ve Çözümler, Seçenekler İletişim Kutusu
Bu iletişim kutusunu tanımlamanızı sağlar [!INCLUDE[vcprvc](../../code-quality/includes/vcprvc_md.md)] yapı ve proje günlüğü, performans ve dosya türleri desteklemek için ilgili ayarlar.

### <a name="to-access-this-dialog-box"></a>Bu iletişim kutusuna erişmek için

1.  Üzerinde **Araçları** menüsünü tıklatın **seçenekleri**.

2.  Seçin **projeler ve çözümler**ve ardından **VC ++ proje ayarları**.

## <a name="build-logging"></a>Günlük kaydı oluşturun
 **Evet**

  Derleme günlük dosyasının oluşturulmasını etkinleştirir. Bu seçeneği projenin Ara dosyaları dizininde bulunan BuildLog.htm üretir. Her yeni derleme önceki BuildLog.htm dosyanın üzerine yazar.

 **Yok**

  Derleme günlüğü dosyası oluşturulmasını devre dışı bırakır.

## <a name="show-environment-in-log"></a>Günlükte ortamı Göster
 **Evet**

 Derleme günlüğü dosyası ortam değişkenleri listeler. Bu seçenek, tüm ortam değişkenleri, oluşumunu sırasında yantısılmayacağını belirtir [!INCLUDE[vcprvc](../../code-quality/includes/vcprvc_md.md)] projelere derleme günlüğü dosyası.

 **Yok**

 Ortam değişkenleri derleme günlük dosyasından hariç tutun.

## <a name="build-timing"></a>Zamanlama oluşturma
 **Evet**

  Derleme zamanlaması üzerinde kapatır. Seçili olduğunda, derleme tamamlamak geçen süre için çıkış penceresine gönderilir. Daha fazla bilgi için [çıkış penceresine](../../ide/reference/output-window.md).

 **Yok**

 Derleme zamanlaması devre dışı bırakır.

## <a name="maximum-concurrent-c-compilations"></a>En fazla eşzamanlı C++ derlemesi
  En fazla paralel C++ derlemesi için kullanılacak CPU çekirdeği sayısını belirtir.

## <a name="extensions-to-include"></a>Dahil etmek için uzantıları
  Projenize unity'nin dosyalarının dosya adı uzantılarını belirtir.

## <a name="extensions-to-hide"></a>Gizlenecek uzantılar
  İçinde görüntülenmeyecek dosyalarının dosya adı uzantılarını belirtir **Çözüm Gezgini** olduğunda **tüm dosyaları göster** etkinleştirilir.

## <a name="build-customization-search-path"></a>Derleme özelleştirme arama yolu
  Yardımcı .rules dosyaları içeren dizinler listesini tanımlamak projeleriniz için derleme kuralları belirtir.

## <a name="solution-explorer-mode"></a>Çözüm Gezgini modu
 **Projede sadece dosyaları göster**

  Yapılandırır **Çözüm Gezgini** sadece projedeki dosyaları görüntülemek için.

 **tüm dosyaları göster**

  Yapılandırır **Çözüm Gezgini** diskteki proje klasöründeki dosya ve proje dosyaları göstermek için.

## <a name="enable-project-caching"></a>Proje önbelleğe almayı etkinleştir
**Evet**

Projeyi sonraki açtığınızda, proje dosyalarından yeniden hesaplama yerine verileri önbelleğe yükleyebilir, böylece Visual Studio Proje verileri önbelleğe almak için etkinleştirir. Önbelleğe alınan verileri kullanarak proje yükleme süresini önemli ölçüde hızlandırabilirsiniz.

**Yok**

Önbelleğe alınmış proje verilerini kullanmayın. Her proje yükler proje dosyaları ayrıştırılamıyor.

## <a name="see-also"></a>Ayrıca bkz.

- [C/C++ Programları Oluşturma](/cpp/build/building-c-cpp-programs)
- [C/C++ Derleme Başvurusu](/cpp/build/reference/c-cpp-building-reference)