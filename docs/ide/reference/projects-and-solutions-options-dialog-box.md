---
title: Projeler ve çözümler, Seçenekler iletişim kutusu
ms.date: 07/26/2019
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Projects.General
helpviewer_keywords:
- Projects and Solutions Options dialog box
- Options dialog box, Projects and Solutions
ms.assetid: 2801f24e-a138-488a-ae3c-e1f99a678ac0
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 37d31f76a448933bb3809cd609ebd355c8e0a04b
ms.sourcegitcommit: ce1ab8a25c66a83e60eab80ed8e1596fe66dd85c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/29/2019
ms.locfileid: "68605958"
---
# <a name="options-dialog-box-projects-and-solutions--general"></a>Seçenekler iletişim kutusu: Projeler ve çözümler \> genel

Visual Studio 'nun projelerle ve çözümlerle ilgili davranışını tanımlamak için bu sayfayı kullanın. Bu seçeneklere erişmek için **Araçlar** > **Seçenekler**, **Projeler ve çözümler**' i seçin ve ardından **genel**' i seçin.

**Genel** sayfasında aşağıdaki seçenekler bulunur.

## <a name="always-show-error-list-if-build-finishes-with-errors"></a>Derleme hatalarla sonlandıysanız her zaman Hata Listesi göster

Yapı tamamlamada **hata listesi** penceresini açar, yalnızca bir proje derlenbir şekilde başarısız olursa. Oluşturma işlemi sırasında oluşan hatalar görüntülenir. Bu seçenek kaldırıldığında hatalar yine oluşur ancak yapı tamamlandığında pencere açılmaz. Bu seçenek varsayılan olarak etkindir.

## <a name="track-active-item-in-solution-explorer"></a>Çözüm Gezgini etkin öğeyi izle

Seçildiğinde, **Çözüm Gezgini** otomatik olarak açılır ve etkin öğe seçilir. Seçilen öğe, bir proje veya çözümde farklı dosyalarla veya bir tasarımcıda farklı bileşenlere çalışırken değişir. Bu seçenek temizlenmiş olduğunda **Çözüm Gezgini** seçimi otomatik olarak değişmez. Bu seçenek varsayılan olarak etkindir.

## <a name="show-advanced-build-configurations"></a>Gelişmiş derleme yapılandırmasını göster

Seçildiğinde, derleme yapılandırma seçenekleri **Proje özellik sayfaları** iletişim kutusunda ve **Çözüm Özellik sayfaları** iletişim kutusunda görünür. Temizlenme sırasında, derleme yapılandırma seçenekleri **Proje özellik sayfaları** iletişim kutusunda ve bir yapılandırma ya da iki yapılandırma içeren Visual Basic ve C# projeler için **Çözüm Özellik sayfaları** iletişim kutusu üzerinde görünmez Hata Ayıkla ve serbest bırak. Bir projede Kullanıcı tanımlı bir yapılandırma varsa, derleme yapılandırma seçenekleri gösterilir.

Bu seçilmediğinde, derleme için derleme **çözümü**, **çözümü yeniden derleme**ve  **çözümü Temizleme**gibi komutlar, sürüm yapılandırmasında ve başlatma gibi **hata ayıklama** menüsündeki komutlarda gerçekleştirilir.  **Hata ayıklama ve hata** ayıklama **olmadan başlatma**, hata ayıklama yapılandırmasında gerçekleştirilir.

## <a name="always-show-solution"></a>Çözümü her zaman göster

Seçildiğinde, çözüm ve çözümler üzerinde işlem yapan tüm komutlar her zaman IDE 'de gösterilir. Temizlenme sırasında, tüm projeler tek başına projeler olarak oluşturulur ve çözüm yalnızca bir proje içeriyorsa IDE 'deki çözümler üzerinde çalışan Çözüm Gezgini veya komutlarda çözümü görmezsiniz.

::: moniker range="vs-2017"

## <a name="save-new-projects-when-created"></a>Oluşturulduğunda yeni projeleri Kaydet

Seçildiğinde, **Yeni proje** iletişim kutusunda projeniz için bir konum belirtebilirsiniz. Kaldırıldığında, tüm yeni projeler geçici proje olarak oluşturulur. Geçici projelerle çalışırken bir disk konumu belirtmek zorunda kalmadan bir proje oluşturup deneyebilirsiniz.

::: moniker-end

## <a name="warn-user-when-the-project-location-is-not-trusted"></a>Proje konumu güvenilir olmadığında kullanıcıyı uyar

Yeni bir proje oluşturmaya veya var olan bir projeyi tam güvenilir olmayan bir konumda açmaya çalışırsanız (örneğin, bir UNC yolu veya HTTP yolu üzerinde), bir ileti görüntülenir. Tam güvenilir olmayan bir konumda bir projeyi oluşturma veya açma girişiminde bulunan her seferinde iletinin görüntülenip görüntülenmeyeceğini belirtmek için bu seçeneği kullanın.

## <a name="show-output-window-when-build-starts"></a>Derleme başladığında çıkış penceresini göster

, [Çıkış penceresini](../../ide/reference/output-window.md) otomatik olarak IDE 'de, çözüm derlemelerinin bilinemeyebilir öğesinde görüntüler.

## <a name="prompt-for-symbolic-renaming-when-renaming-files"></a>Dosyaları yeniden adlandırırken sembolik yeniden adlandırma iste

Seçildiğinde, Visual Studio projedeki tüm başvuruları kod öğesine de yeniden adlandırmasının gerekip gerekmediğini soran bir ileti kutusu görüntüler.

## <a name="prompt-before-moving-files-to-a-new-location"></a>Dosyaları yeni bir konuma taşımadan önce sor

Seçildiğinde, dosya konumları **Çözüm Gezgini**eylemler tarafından değiştirilmeden önce Visual Studio bir onay iletisi kutusu görüntüler.

## <a name="reopen-documents-on-solution-load"></a>Çözüm yükünden belgeleri yeniden aç

**Visual Studio 2017 sürüm 15,8 ' de tanıtılan**

Seçildiğinde, çözüm açıldığında kalan bir önceki sefer açık olan belgeler otomatik olarak açılır.

Belirli dosya veya tasarımcı türlerini yeniden açmak çözüm yükünü geciktirebilirler. Çözümün önceki bağlamını geri yüklemek istemiyorsanız [çözüm yükleme performansını artırmak](../../ide/visual-studio-performance-tips-and-tricks.md#disable-automatic-file-restore) için bu seçeneğin işaretini kaldırın.

## <a name="see-also"></a>Ayrıca bkz.

- [Seçenekler iletişim kutusu: Projeler ve çözüm \> konumları](projects-solutions-locations-options.md)
- [Seçenekler Iletişim kutusu, projeler ve çözümler, derleme ve çalıştırma](../../ide/reference/options-dialog-box-projects-and-solutions-build-and-run.md)
- [Seçenekler İletişim Kutusu, Projeler ve Çözümler, Web Projeleri](../../ide/reference/options-dialog-box-projects-and-solutions-web-projects.md)
