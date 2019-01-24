---
title: 'Nasıl yapılır: El ile bir uzantı (VSIX dağıtımı) paketi | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: devlang-csharp
ms.topic: conceptual
ms.assetid: d25990e0-e782-4a79-9d9a-1caf3c56c6a2
caps.latest.revision: 10
manager: jillfra
ms.openlocfilehash: 3537879481430490d32ab30f8f6a2f9f7353659b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54773589"
---
# <a name="how-to-manually-package-an-extension-vsix-deployment"></a>Nasıl yapılır: El ile bir uzantı (VSIX dağıtımı) paketi
Sarmak için bir VSIX paketi oluşturmak bir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] dağıtım için uzantısı. Paketi oluşturmak için üç yolu vardır:  
  
- Dahil edilen genişletilebilirlik şablonlarından birini kullanarak bir VSIX paket projesi oluşturun [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] SDK. Bu, çoğu senaryo için en kolay seçenektir.  
  
- İçinde boş bir uzantı projenizin çıktısını kaydırma [VSIX projesi](../extensibility/vsix-project-template.md). Şablonları, desteklenmeyen derlemelerini ve özel türler için bu seçeneği öneririz.  
  
- El ile bir VSIX paketi oluşturun. Yalnızca diğer iki seçenek kullanılabilir olmadığında bu seçeneği öneririz.  
  
  Bu belgede, üçüncü bir seçenek açıklanmaktadır.  
  
## <a name="creating-a-vsix-package"></a>VSIX paketi oluşturma  
 El ile bir uzantı paketini için extension.manifest dosya ve uzantı projesini bir [Content_Types] .xml dosyasına koymak bunları derleme çıkışınızı birlikte sıkıştırılmış bir dosya ekleyin ve böylece bir .vsix dosya adı uzantısına sahip sıkıştırılmış dosyayı yeniden adlandırın. Paketlenmiş uzantı tarafından desteklenen bir türde olmalıdır [VSIX şema](http://msdn.microsoft.com/76e410ec-b1fb-4652-ac98-4a4c52e09a2b).  
  
> [!NOTE]
>  VSIX paketlerini dosyaların adları boşluk içermemelidir ya da devre dışı olarak Tekdüzen Kaynak Tanımlayıcıları (URI) içinde ayrılmış karakterleri tanımlanan altında [ \[RFC2396\]](http://go.microsoft.com/fwlink/?LinkId=90339).  
  
#### <a name="to-manually-create-a-vsix-package"></a>El ile bir VSIX paketi oluşturmak için  
  
1.  VSIX şema tarafından desteklenen bir tür için bir Visual Studio uzantısı oluşturun.  
  
2.  Bir XML dosyası oluşturun ve adlandırın `extension.vsixmanifest`.  
  
3.  VSIX şema göre extension.vsixmanifest dosyasındaki doldurun. Bir örnek listesi için bkz. [PackageManifest öğesi (kök öğe, VSX şema)](http://msdn.microsoft.com/f8ae42ba-775a-4d2b-976a-f556e147f187).  
  
4.  İkinci bir XML dosyası oluşturun ve adlandırın `[Content_Types].xml`.  
  
5.  [Content_Types] .xml dosyasını belirtildiği gibi doldurun [Content_types yapısı\].xml dosyası](../extensibility/the-structure-of-the-content-types-dot-xml-file.md).  
  
6.  Her iki XML dosyaları dağıtılacak uzantısı ile birlikte bir dizine yerleştirin.  
  
     Bir proje şablonu veya öğe şablonu söz konusu olduğunda, XML dosyaları ile aynı klasörde şablonu içeren .zip dosyasını yerleştirin. XML dosyaları .zip dosyasına yerleştirmeniz gerekir.  
  
     Diğer durumlarda, XML dosyalarını yapı çıkışını aynı dizine koyun.  
  
7.  Windows Gezgini'nde, içerik uzantısı içeren klasörü ve iki XML dosyasını sağ tıklayın, **göndermek için**ve ardından **sıkıştırılmış (daraltılmış) klasör**.  
  
8.  Sonuçta elde edilen .zip dosyası olarak yeniden adlandırın *Filename*.vsix, burada *Filename* paketinizi yükleyen yeniden dağıtılabilir dosya adıdır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio uzantıları gönderme](../extensibility/shipping-visual-studio-extensions.md)   
 [Bir VSIX paketinin anatomisi](../extensibility/anatomy-of-a-vsix-package.md)   
 [PackageManifest öğesi (kök öğe, VSX Şeması)](http://msdn.microsoft.com/f8ae42ba-775a-4d2b-976a-f556e147f187)