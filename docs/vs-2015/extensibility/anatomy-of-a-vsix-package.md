---
title: Bir VSIX paketinin anatomisi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- visual studio extension
- vsix
- packages
ms.assetid: 8b86d62f-c274-4e91-82e0-38cdb9a423d5
caps.latest.revision: 16
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 86c2beeab5fba0224fbdfb104d01ee5c28bba158
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65699139"
---
# <a name="anatomy-of-a-vsix-package"></a>Bir VSIX Paketinin Anatomisi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir VSIX paketi bir veya daha fazla Visual Studio uzantıları, sınıflandırmak ve uzantıları yüklemek için Visual Studio kullanan meta veriler ile birlikte içeren bir .vsix dosyasıdır. Bu meta veri, VSIX bildirimi ve [Content_Types] .xml dosyasının içinde yer alır. Bir VSIX paketi, ayrıca yerelleştirilmiş Kurulum metninde sağlamak için bir veya daha fazla Extension.vsixlangpack dosyalar içerebilir ve bağımlılıklarını yüklemek için ek VSIX paketleri içerebilir.  
  
 VSIX paket biçimi açık paketleme kuralları (OPC) standart izler. Paket ikili dosyalarını içerir ve destekleyen dosyaları, birlikte [Content_Types] .xml dosyası ve bir .vsix bildirim dosyası. Bir VSIX paketi birden çok proje veya kendi bildirimleri olan bile birden çok paketleri çıktısını içerebilir.  
  
> [!NOTE]
> VSIX paketlerinde dosyalarının adlarını boşluklar içermemelidir ya da devre dışı olarak Tekdüzen Kaynak Tanımlayıcıları (URI) içinde ayrılmış karakterleri tanımlanan altında [ \[RFC2396\]](http://go.microsoft.com/fwlink/?LinkId=90339).  
  
## <a name="the-vsix-manifest"></a>VSIX bildirimi  
 VSIX bildirimi uzantının yüklenmesini ve aşağıdaki VSX şeması hakkında bilgi içerir. Daha fazla bilgi için [VSIX Uzantı Şeması 1.0 başvurusu](https://msdn.microsoft.com/76e410ec-b1fb-4652-ac98-4a4c52e09a2b). Bir örnek VSIX bildirimi için bkz: [PackageManifest öğesi (kök öğe, VSX şema)](https://msdn.microsoft.com/f8ae42ba-775a-4d2b-976a-f556e147f187).  
  
 VSIX bildirimi adlandırılmalıdır `extension.vsixmanifest` ne zaman, bir .vsix dosyasına eklenir.  
  
## <a name="the-content"></a>İçeriği  
 Bir VSIX paketi şablonları, araç kutusu öğelerini, VSPackages veya başka tür bir Visual Studio tarafından desteklenen uzantısı içerebilir.  
  
## <a name="language-packs"></a>Dil Paketleri  
 Bir VSIX paketi bir kez veya yükleme sırasında yerelleştirilmiş metin sağlamak için daha fazla Extension.vsixlangpack dosyaları içerebilir. Daha fazla bilgi için [VSIX paketlerini yerelleştirme](../extensibility/localizing-vsix-packages.md).  
  
## <a name="dependencies-and-references"></a>Bağımlılıklar ve başvuruları  
 Bir VSIX paketi diğer VSIX paketleri başvuru olarak içerebilir. Her diğer bu paketlerin kendi VSIX bildirimi eklemeniz gerekir.  
  
 Bir kullanıcı, bağımlılıklara sahip bir uzantıyı yüklemeye çalışırsa, yükleyici, gerekli derlemeleri kullanıcı sistemde yüklü olduğunu doğrular. Gerekli derlemeleri bulunmazsa, **Uzantılar ve güncelleştirmeler** eksik derlemelerin bir listesini görüntüler.  
  
 Bir veya daha fazla uzantı bildirimi içeriyorsa, [başvuru](https://msdn.microsoft.com/32c52934-e81e-4b53-8cb6-4df45ef7bfa8) öğeleri **Uzantılar ve güncelleştirmeler** sistemde yüklü uzantıları her başvurunun bildirimi karşılaştırır ve yükler Başvurulan uzantı zaten yüklü değilse. Başvurulan uzantı önceki bir sürümü yüklüyse, yeni sürümü değiştirir.  
  
 Birden çok proje çözümde bir proje, aynı çözümdeki başka bir projeye bir başvuru içeriyorsa, proje bağımlılıklarını VSIX paketini içerir. Başvuru iç projesi için ve ardından tıklayarak bu davranışı geçersiz kılabilirsiniz **özellikleri** ayarlama penceresinde **çıktı grupları dahil vsıx'te** özelliğini `BuiltProjectOutputGroup`.  
  
 Başvurulan derlemelerden Uydu DLL'leri VSIX paketinde eklemek için Ekle `SatelliteDllsProjectOutputGroup` için **çıktı grupları dahil vsıx'te** özelliği.  
  
## <a name="installation-location"></a>Yükleme Konumu  
 Yükleme sırasında **Uzantılar ve güncelleştirmeler** % LocalAppData%\Microsoft\VisualStudio\14.0\Extensions altında bir klasöre VSIX paketinin içeriği arar.  
  
 Bir kullanıcıya özgü dizin % LocalAppData % olduğu için varsayılan olarak, yüklemeyi yalnızca geçerli kullanıcı için geçerlidir. Ancak ayarlarsanız [AllUsers](https://msdn.microsoft.com/ac817f50-3276-4ddb-b467-8bbb1432455b) için bildirimin öğesi `True`, uzantı altında yüklü... \\ *VisualStudioInstallationFolder*\Common7\IDE\Extensions ve bilgisayarın tüm kullanıcıları için kullanılabilir olacak.  
  
## <a name="contenttypesxml"></a>[Content_Types] .xml  
 [Content_Types] .xml dosyasının genişletilmiş .vsix dosyasını dosya türlerini tanımlar. Visual Studio Paket yüklemesi sırasında bu dosyayı kullanır ancak dosyayı yüklemez. Bu dosya hakkında daha fazla bilgi için bkz. [Content_types yapısı\].xml dosyası](../extensibility/the-structure-of-the-content-types-dot-xml-file.md).  
  
 [Content_Types] .xml dosyasının açık paketleme kuralları (OPC tarafından) standart gereklidir. OPC hakkında daha fazla bilgi için bkz: [OPC: Bir yeni standart için paketleme verilerinizi](http://go.microsoft.com/fwlink/?LinkID=148207) MSDN Web sitesinde.
