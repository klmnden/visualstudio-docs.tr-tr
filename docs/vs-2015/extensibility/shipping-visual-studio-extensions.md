---
title: Uzantıları gönderme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- VSIX deployment
- deployment, VSIX
- satellite DLLs, in VSIX packages
ms.assetid: 13cd263d-25f7-488e-9c1a-cff908caedb6
caps.latest.revision: 29
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: ed8080b8e470276a38fbf300edbf801dc8e141fd
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54785268"
---
# <a name="shipping-visual-studio-extensions"></a>Visual Studio Uzantıları Gönderme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

**Not**: Visual Studio Galerisi, Visual Studio Market tarafından değiştirilmektedir. Ayrıntılar için bu konunun en son sürümüne bakın.


Uzantınızı geliştirme bitirdikten sonra diğer makinelere yükleyin, arkadaşlarınız ve iş arkadaşları ile paylaşma veya Visual Studio galerisinde yayımlamak. Bu bölümde biz yayımlama ve uzantınızı sağlamak için yapmanız gereken her şeyi açıklayan: yayımlama, yerelleştirme ve güncelleştirme .vsix dosyaları ile çalışma.

## <a name="working-with-vsix-extensions"></a>VSIX uzantıları ile çalışma
 Boş bir VSIX projesi oluşturarak ve farklı öğe şablonları ekleyerek, bir VSIX uzantılarını oluşturabilirsiniz. Daha fazla bilgi için [VSIX proje şablonu](../extensibility/vsix-project-template.md).

 Paket proje şablonları, öğe şablonları, VSPackage'ları, Yönetilen Genişletilebilirlik Çerçevesi (MEF) bileşenleri için VSIX biçimi kullanabileceğiniz **araç kutusu** denetimleri, derlemeleri ve özel türler (Bu içerir özel başlangıç sayfaları). VSIX biçimi, dosya tabanlı dağıtım kullanır. VSIX paketleri hakkında daha fazla bilgi için bkz. [bir VSIX paketinin anatomisi](../extensibility/anatomy-of-a-vsix-package.md).

 VSIX biçimi, kod parçacıkları yüklenmesini desteklemez. Genel Derleme Önbelleği (GAC) için veya sistem kayıt defterine yazma gibi diğer bazı senaryolar da desteklemez. GAC veya kayıt defterinde yükleme için yazmanız gereken Windows Yükleyici kullanmanız gerekir. Daha fazla bilgi için [hazırlama uzantıları için Windows Installer dağıtımı](../extensibility/preparing-extensions-for-windows-installer-deployment.md).

## <a name="publishing-your-extension-to-the-visual-studio-gallery"></a>Uzantınız için Visual Studio Galerisine yayımlama
 Yalnızca bir sunucuya yerleştirmeyi ya da bunları .vsix dosyasını posta tarafından uzantınızı diğer kişilere dağıtabilirsiniz. Ancak birçok kişinin elinizde kodunuzu almak için en iyi yolu, yerleştirip [Visual Studio Galerisi](http://go.microsoft.com/fwlink/?LinkID=123847). Uzantılar Visual Studio Galerisi aracılığıyla Visual Studio kullanıcılara kullanılabilir **Uzantılar ve güncelleştirmeler**. Daha fazla bilgi için [bulma ve Visual Studio uzantılarını kullanarak](../ide/finding-and-using-visual-studio-extensions.md).

 Bir uzantıyı karşıya yüklemek için Visual Studio Galerisine gösteren tam bir örnek için bkz. [izlenecek yol: Visual Studio uzantısı yayımlama](../extensibility/walkthrough-publishing-a-visual-studio-extension.md).

## <a name="private-galleries"></a>Özel Galeriler
 Denetimleri, şablonlar ve araçlar geliştirirken, özel bir galeri intranetinizdeki yayınlayarak bunları kuruluşunuzla paylaşabilirsiniz. Daha fazla bilgi için [özel galeriler](../extensibility/private-galleries.md).

## <a name="localizing-your-extension"></a>Uzantınızı yerelleştirme
 Uzantınızı farklı yerel ayarlar yayın planlıyorsanız, yerelleştirme düşünmelisiniz. Nelerin dahil açıklaması için bkz [VSIX paketlerini yerelleştirme](../extensibility/localizing-vsix-packages.md).

## <a name="updating-and-versioning-your-extension"></a>Güncelleştirme ve sürüm oluşturma uzantınızı
 Uzantınızı yayımladıktan sonra var gelen güncelleştirmeniz gerektiğinde bir süre. Visual Studio galeride yayımlanmış uzantı güncelleştirileceğini öğrenmek için bkz: [nasıl yapılır: Uzantı güncelleştirmesi](../extensibility/how-to-update-a-visual-studio-extension.md).

 Uzantınızı Visual Studio'nun birden çok sürümünü destekleyecek şekilde ayarlayabilirsiniz. Daha fazla bilgi için [destekleyen birden çok Versions of Visual Studio](../extensibility/supporting-multiple-versions-of-visual-studio.md).

## <a name="related-topics"></a>İlgili Konular

|Başlık|Açıklama|
|-----------|-----------------|
|[VSIX Proje Şablonunu Kullanmaya Başlama](../extensibility/getting-started-with-the-vsix-project-template.md)|VSIX proje şablonunu özel proje şablonunu yüklemek için nasıl kullanılacağını açıklar.|
|[Bir VSIX Paketinin Anatomisi](../extensibility/anatomy-of-a-vsix-package.md)|Bir VSIX paketi bileşenlerinin açıklar.|
|[VSIX Proje Şablonu](../extensibility/vsix-project-template.md)|Paketleme ve uzantı yayımlamak hakkında adım adım yönergeler sağlar.|
|[VSIX Paketlerini Yerelleştirme](../extensibility/localizing-vsix-packages.md)|Yerelleştirilmiş metin extension.vsixlangpack dosyalarını kullanarak yükleme işlemini sağlamayı açıklar.|
|[Nasıl yapılır: Bir uzantıyı güncelleştir](../extensibility/how-to-update-a-visual-studio-extension.md)|Sisteminizde bir uzantı güncelleştirme ve var olan bir Visual Studio uzantısı için bir güncelleştirme dağıtmayı açıklar.|
|[Nasıl yapılır: VSIX paketine bağımlılık ekleme](../extensibility/how-to-add-a-dependency-to-a-vsix-package.md)|VSIX dağıtım paketleri başvurularını eklemeyi açıklar.|
|[Uzantıları Windows Installer Dağıtımı için Hazırlama](../extensibility/preparing-extensions-for-windows-installer-deployment.md)|Windows Installer ile uzantınızı dağıtma işlemi açıklanmaktadır.|
|[VSIX Paketlerini İmzalama](../extensibility/signing-vsix-packages.md)|VSIX paketlerini imzalama açıklanmaktadır.|
|[Özel Galeriler](../extensibility/private-galleries.md)|Özel galeriler uzantıları için nasıl oluşturulacağını açıklar.|
|[Visual Studio'nun Birden Çok Sürümünü Destekleme](../extensibility/supporting-multiple-versions-of-visual-studio.md)|Uzantı destek sağlamak nasıl Visual Studio'nun birden çok sürümünü gösterir.|
