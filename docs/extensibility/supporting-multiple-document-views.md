---
title: Birden çok belge görünümünü destekleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], custom - multiple document views
ms.assetid: c7ec2366-91c4-477f-908d-e89068bdb3e3
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 93d4e2a307a6bdd8f06b928103c38337497b7a95
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66353476"
---
# <a name="supporting-multiple-document-views"></a>Birden Çok Belge Görünümünü Destekleme
Düzenleyiciniz için ayrı bir belge verileri ve belge görünümü nesneleri oluşturarak, bir belgenin birden fazla görünümü sağlayabilirsiniz. Ek belge görünümü yararlı olabilecek bazı durumlar şunlardır:

- Yeni pencere desteği: Düzenleyicide açık bir pencere zaten olan bir kullanıcı seçerek yeni bir pencere açabilmek düzenleyiciniz aynı türde iki veya daha fazla görünümlerini sağlamak istediğiniz **yeni pencere** komutunu **penceresi** menüsü.

- Form ve kod görünümü desteği: Farklı görünümlerini sağlamak için düzenleyici kullanmanız gerekir. [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)], örneğin, bir form görünümü hem de bir kod görünümü sağlar.

  Bunun hakkında daha fazla bilgi için Visual Studio Paket şablon tarafından oluşturulan özel düzenleyici proje EditorFactory.cs dosyasında CreateEditorInstance yordamına bakın. Bu proje hakkında daha fazla bilgi için bkz. [izlenecek yol: Bir özel düzenleyici oluşturma](../extensibility/walkthrough-creating-a-custom-editor.md).

## <a name="synchronizing-views"></a>Eşitleme görünümleri
 Birden çok görünüm uyguladığınızda, belge veri nesnesinin veri ile eşitlenen tüm görünümleri tutmak için sorumludur. Olay arabirimleri üzerinde işleme kullanabileceğiniz <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer> verilerle birden çok görünüm eşitlenecek.

 Kullanmıyorsanız, <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer> belge veri nesnesine yapılan değişiklikleri işlemek için kendi olay sistemi uygulamalıdır. daha sonra birden çok görünüm eşitlenecek nesne. Farklı ayrıntı düzeyleri, birden çok görünüm güncel tutmak için kullanabilirsiniz. Tek bir görünümde yazarken maksimum ayrıntı düzeyinin ayarıyla diğer görünümleri hemen güncelleştirilir. Bunlar etkinleştirilene kadar en düşük ayrıntı düzeyiyle diğer görünümleri güncelleştirilmez.

## <a name="determining-whether-document-data-is-already-open"></a>Zaten açık olan belge verileri olup olmadığını belirleme
 Tümleşik geliştirme ortamında (IDE) çalıştırılan Belge tablosu (RDT), verileri bir belgenin zaten Aşağıdaki diyagramda gösterildiği gibi açık olup olmadığını izlemek yardımcı olur.

 ![DocDataView grafiği](../extensibility/media/docdataview.gif "Docdataview") birden çok görünüm

 Varsayılan olarak her görünümün (belge görünümü nesnesi) kendi pencere çerçevesinde kapsanan (<xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame>). Daha önce belirtildiği gibi ancak belge verileri birden çok görünüm görüntülenebilir. Bunu etkinleştirmek için Visual Studio RDT söz konusu belge zaten bir düzenleyicide açık olup olmadığını belirlemek için denetler. IDE çağırdığında <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A> düzenleyici oluşturmak için boş olmayan bir değer döndürdü `punkDocDataExisting` parametresi belge zaten başka bir düzenleyicide açık olduğunu gösterir. RDT işlevleri hakkında daha fazla bilgi için bkz: [çalıştırılan Belge tablosu](../extensibility/internals/running-document-table.md).

 İçinde <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory> uygulama, döndürülen belge veri nesnesini inceler `punkDocDataExisting` belge verileri düzenleyiciniz için uygun olup olmadığını belirlemek için. (Örneğin, yalnızca HTML veri bir HTML düzenleyicisi tarafından görüntülenmesi gerekir.) Uygun değilse, düzenleyici fabrikası ikinci bir görünüm için veriler sağlamalıdır. Varsa `punkDocDataExisting` parametresi `NULL`, ya da mümkündür belge veri nesnesi başka bir düzenleyicide Aç ya da, büyük olasılıkla, belge verileri zaten farklı bir görünüm aynı Düzenleyici içinde açık olduğunu. Belge verilerini, düzenleyici fabrikası desteği olmayan farklı bir düzenleyicide açık ise, Visual Studio Düzenleyicisi Fabrika açmak başarısız. Daha fazla bilgi için [nasıl yapılır: Belge verilerine görünüm ekleme](../extensibility/how-to-attach-views-to-document-data.md).