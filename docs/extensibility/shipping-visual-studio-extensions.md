---
title: Visual Studio uzantıları gönderme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSIX deployment
- deployment, VSIX
- satellite DLLs, in VSIX packages
ms.assetid: 13cd263d-25f7-488e-9c1a-cff908caedb6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2ea2217614ed27a98281cce7a3d34b72f74ae803
ms.sourcegitcommit: 1c8e07b98fc0a44b5ab90bcef77d9fac7b3eb452
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/25/2019
ms.locfileid: "56796601"
---
# <a name="shipping-visual-studio-extensions"></a>Visual Studio Uzantıları Gönderme
Uzantınızı geliştirme bitirdikten sonra diğer makinelere yükleyin, arkadaşlarınız ve iş arkadaşları ile paylaşma veya Visual Studio Market'te yayımlayın. Bu bölümde biz yayımlama ve uzantınızı sağlamak için yapmanız gereken her şeyi açıklayan: yayımlama, yerelleştirme ve güncelleştirme .vsix dosyaları ile çalışma.

## <a name="working-with-vsix-extensions"></a>VSIX uzantıları ile çalışma
 Boş bir VSIX projesi oluşturarak ve farklı öğe şablonları ekleyerek, bir VSIX uzantılarını oluşturabilirsiniz. Daha fazla bilgi için [VSIX proje şablonu](../extensibility/vsix-project-template.md).

 Paket proje şablonları, öğe şablonları, VSPackage'ları, Yönetilen Genişletilebilirlik Çerçevesi (MEF) bileşenleri için VSIX biçimi kullanabileceğiniz **araç kutusu** denetimleri, derlemeleri ve özel türler (Bu içerir özel başlangıç sayfaları için görseli Studio 2017 için). VSIX biçimi, dosya tabanlı dağıtım kullanır. VSIX paketleri hakkında daha fazla bilgi için bkz. [bir VSIX paketinin anatomisi](../extensibility/anatomy-of-a-vsix-package.md).

 VSIX biçimi, kod parçacıkları yüklenmesini desteklemez. Genel Derleme Önbelleği (GAC) için veya sistem kayıt defterine yazma gibi diğer bazı senaryolar da desteklemez. GAC veya kayıt defterinde yükleme için yazmanız gereken Windows Yükleyici kullanmanız gerekir. Daha fazla bilgi için [hazırlama uzantıları için Windows Installer dağıtımı](../extensibility/preparing-extensions-for-windows-installer-deployment.md).

## <a name="publishing-your-extension-to-the-visual-studio-marketplace"></a>Uzantınızı Visual Studio Market'te yayımlama
 Yalnızca bir sunucuya yerleştirmeyi ya da bunları .vsix dosyasını posta tarafından uzantınızı diğer kişilere dağıtabilirsiniz. Ancak birçok kişinin elinizde kodunuzu almak için en iyi yolu, yerleştirip [Visual Studio Market](https://marketplace.visualstudio.com/vs). Visual Studio Market uzantıları aracılığıyla Visual Studio kullanıcılara kullanılabilir **Uzantılar ve güncelleştirmeler**. Daha fazla bilgi için [bulma ve Visual Studio uzantılarını kullanarak](../ide/finding-and-using-visual-studio-extensions.md).

 Visual Studio Market'te uzantı yüklemeyi gösteren bir tam örnek için bkz: [izlenecek yol: Visual Studio uzantısı yayımlama](../extensibility/walkthrough-publishing-a-visual-studio-extension.md).

## <a name="private-galleries"></a>Özel Galeriler
 Denetimleri, şablonlar ve araçlar geliştirirken, özel bir galeri intranetinizdeki yayınlayarak bunları kuruluşunuzla paylaşabilirsiniz. Daha fazla bilgi için [özel galeriler](../extensibility/private-galleries.md).

## <a name="localizing-your-extension"></a>Uzantınızı yerelleştirme
 Uzantınızı farklı yerel ayarlar yayın planlıyorsanız, yerelleştirme düşünmelisiniz. Nelerin dahil açıklaması için bkz [VSIX paketlerini yerelleştirme](../extensibility/localizing-vsix-packages.md).

## <a name="updating-and-versioning-your-extension"></a>Güncelleştirme ve sürüm oluşturma uzantınızı
 Uzantınızı yayımladıktan sonra var gelen güncelleştirmeniz gerektiğinde bir süre. Visual Studio Market'te yayımlanmış bir uzantıyı güncelleştirmek nasıl öğrenmek için bkz: [nasıl yapılır: Uzantı güncelleştirmesi](../extensibility/how-to-update-a-visual-studio-extension.md).

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
|[Visual Studio'yu Bulma](locating-visual-studio.md)|Özel uzantı dağıtımı için Visual Studio örneklerini bulmak açıklar.|
