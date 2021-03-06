---
title: VSIX bildirim Tasarımcısı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- VS.Sdk.VsixManifestEditor
helpviewer_keywords:
- vsixmanifest
- vsix manifest
- manifest designer
ms.assetid: 5a691e77-cf91-430d-90ea-361d9031ef83
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7c13d32ab6b91dce94bab307f6bbc6744f9c17a0
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66322848"
---
# <a name="vsix-manifest-designer"></a>VSIX Bildirim Tasarımcısı
Visual Studio uzantısı için yükleme davranışı ayarlayan bir VSIX paket bildirim dosyası, değiştirir.

 **VSIX bildirim Tasarımcısı** temel alınan VSIX şemaya eşler. Her şema öğesi, karşılık gelen bir denetim Tasarımcısı'nda kullanarak ayarlayabilirsiniz. Şeması hakkında daha fazla bilgi için bkz. [VSIX Uzantı Şeması 2.0 başvurusu](../extensibility/vsix-extension-schema-2-0-reference.md).

 Açmak için **VSIX bildirim Tasarımcısı**, bulun bir *source.extension.vsixmanifest* dosyası **Çözüm Gezgini**, dosyasını açın. Bildirim Tasarımcısı dosyayı geçerli XML içermiyorsa açılamaz.

> [!NOTE]
> *Source.extension.vsixmanifest* çıkış dosyası için *extension.vsixmanifest* paketin ne zaman oluşturulur.

## <a name="uielement-list"></a>UIElement listesi
 **VSIX bildirim Tasarımcısı** şemanın en üst düzey bu öğelere karşılık gelen dört bölüm içerir:

- Meta Veriler

- Hedefleri yükle

- Varlıklar

- Bağımlılıklar

  Başlık alanı aşağıdaki denetimleri içerir.

  **Ürün adı** uzantı adı açıklar.

  **Ürün Kimliği** bu paket için benzersiz kimlik bilgilerini belirtir.

  **Yazar** uzantı yazarının adını belirtir.

  **Sürüm** uzantısı sürüm numarasını belirtir.

  **Meta verileri** sekmesi aşağıdaki denetimleri içerir.

  **Açıklama** uzantı görüntülenecek metin açıklamasını sağlar **Uzantı Yöneticisi**.

  **Dil** bildiriminde metinsel verilere karşılık gelen paket varsayılan dilini belirtir. `Language` Özniteliği aşağıdaki ortak dil çalışma zamanı (CLR) yerel kod kurala için kaynak grupları, örneğin, en-us, en, fr-fr. Varsayılan olarak, paketi tüm Visual Studio dil sürümünü çalışacak başka bir deyişle, nötr, değerdir.

  **Lisans** var olan kullanıcı lisansı içeren metin dosyası belirtir.

  **Simge** grafik dosyasını belirtir ( *.png*, *.bmp*, *.jpeg*, *.ico*) görüntülenecek simge içeriyor **Uzantı Yöneticisi**, varsa bir simge. Bu boyutlara yeniden boyutlandırılabilir veya simge görüntüsü 32 x 32 piksel olmalıdır. Simge yok belirtilirse, **Uzantı Yöneticisi** varsayılan bir simge kullanılır.

  **Önizleme görüntüsü** grafik dosyasını belirtir ( *.png*, *.bmp*, *.jpeg*, *.ico*) önizleme görüntüsünü içerir görüntülenmesi **Uzantı Yöneticisi**, bir önizleme görüntüsü varsa. Önizleme görüntüsü 200 x 200 piksel olmalıdır. Hiçbir önizleme görüntüsü belirtilirse, **Uzantı Yöneticisi** varsayılan bir görüntü kullanır.

  **Etiketleri** arama ipuçları için kullanılacak metni etiketleri ekler.

  **Sürüm Notları** belirtir ( *.txt*, *.rtf*), sürüm notlarını içerir. Ayrıca sürüm notlarını görüntüleyen bir Web sitesinin URL'sini alır.

  **Başlarken Kılavuzu** belirtir ( *.txt*, *.rtf*) içeriğin veya uzantısı VSIX paketinde kullanma hakkında bilgiler içerir. Bu kılavuz, uzantı yüklemesi tamamlandığında görünür. Ayrıca Kılavuzu görüntüleyen bir Web sitesinin URL'sini alır.

  **Daha fazla bilgi URL'si** ürün hakkında ek bilgi içeren bir Web sitesinin URL'sini belirtir.

  **Hedefleri Yükle** sekmesi aşağıdaki denetimleri içerir.

  **Yükleme türünü** listeler **Visual Studio Uzantısı** ve **uzantı SDK'sı** yükleme türlerini hedefleyin. Seçenekler, seçtiğiniz türüne bağlı olarak farklılık gösterir.

  **Visual Studio Uzantısı** listeler **InstallationTarget** öğeleri nasıl paket yüklenebilir ve bu uzantı Visual Studio ürünleri yüklenebilir. Her ürün adı ve sürüm veya sürüm aralığına göre ayrı olarak tanımlanır. Ürün listesine, değiştirilebilir ve silindi. Ad ve bir ürün sürümüne karşılık gelen **kimliği** ve **sürüm** ilişkili öznitelikleri **InstallationTarget** öğesi.

  **Sürüm aralığı** olduğundan [12.0, 14.0] ve aşağıdaki gösterim kullanır:

- [-en düşük sürüm kapsamlı

- ]-en yüksek sürüm kapsamlı

- (-özel en düşük sürüm

- )-en yüksek sürümü özel

- Tek sürüm # - yalnızca belirtilen sürüm

  **Uzantı SDK** belirli bir ürün ve sürümünüz için kapsamlı olmayan genel bir yükleme belirtir. **Hedef Platform tanımlayıcısı** "hedeflediğiniz Windows," gibi bir platform. **Hedef Platform sürümü** gibi 8.0, hedef platform sürümü. **SDK adı** ve **SDK sürümü** adı ve SDK'sı sürüm numarasını sırasıyla.

  **Bu VSIX tüm kullanıcılar için yüklenir (yüklemede bir yükseltme gerektirir)** bu onay kutusunu seçerseniz, uzantı tüm kullanıcılar için yüklenir; Aksi takdirde, yalnızca geçerli kullanıcı için yüklenir.

  **Bu VSIX yüklü Windows Installer tarafından** uzantısı, bu onay kutusunu seçerseniz, Windows Installer tarafından yüklenir ( *.msi* dosya); Aksi takdirde, tipik bir VSIX paketi olarak yüklenir ( *.vsix*  dosyası).

  **Varlıklar** sekmesi aşağıdaki denetimleri içerir.

  **Varlıklar listesi** uzantısı ya da içerik öğeleri tanımlayan varlık öğeleri listeler bu yüzeyleri paketi. Kaynak, türü ve yol tarafından ayrı ayrı her bir uzantı veya içerik öğesi listelenir. Uzantıları ve içerik öğeleri listesine, değiştirilebilir ve silindi. Bir uzantı veya içerik öğenin yolu ve türünü karşılık gelen `Type` ve `Path` ilişkili öznitelikleri `Asset` öğesi. Aşağıdaki türleri bilinmektedir:

- Microsoft.VisualStudio.Package

- Microsoft.VisualStudio.MefComponent

- Microsoft.VisualStudio.ToolboxControl

- Microsoft.VisualStudio.Samples

- Microsoft.VisualStudio.ProjectTemplate

- Microsoft.VisualStudio.ItemTemplate

- Microsoft.VisualStudio.Assembly

- Microsoft.ExtensionSDK

  Ekleme veya düzenleme bir varlık için varlık mevcut çözümde bir proje veya dosya dosya sistemi ve projenin adı olup olmadığını varlık türünü belirtmeniz gerekir. Katıştırılmış kaydedileceği klasörün adını belirtebilirsiniz.

  Ayrıca, kendi türlerinizi oluşturmak ve bunları benzersiz adlar verin.

  **Bağımlılıkları** sekmesi aşağıdaki denetimleri içerir.

  **Adı, kaynak ve sürüm aralığı** bu paket, bağlı olduğu diğer paketleri olan bu paket bağımlılık öğelerini listeler. Bir bağımlılık paket belirtilirse, bu paketi yüklemeden önce yüklenmelidir; Aksi takdirde, bu paketi yüklemeniz gerekir.

  Bağımlılık paketlerini tanımlayıcı adı, sürüm aralığı, kaynak ve nasıl çözümlenmesi bağımlılığı olduğunu tarafından belirtilir. Her bağımlılık paket adı, sürümü ve kaynak tarafından ayrı ayrı listelenir. Bağımlılık paketlerini listeye eklenen, değiştirilebilir ve silindi.

  Tanımlayıcı eşleşmelidir `ID` bağımlılık paket meta özniteliği. Kaynak bir proje geçerli çözüme, şu anda yüklü bir uzantı veya bir dosya olabilir. **Nasıl Çözüldü bağımlılığıdır** ayarı, göreli yolun iç içe geçmiş bir paketin veya bağımlılık için indirme konumunu URL'si olabilir. Kimlik, sürüm ve bağımlılık paketinin çözümleme karşılık `Id`, `Version`, ve `Location` ilişkili öznitelikleri `Dependency` öğesi.

## <a name="see-also"></a>Ayrıca bkz.
- [VSIX Uzantı Şeması 2.0 başvurusu](../extensibility/vsix-extension-schema-2-0-reference.md)
- [Bir VSIX paketinin anatomisi](../extensibility/anatomy-of-a-vsix-package.md)