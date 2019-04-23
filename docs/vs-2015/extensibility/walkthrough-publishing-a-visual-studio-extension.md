---
title: Uzantı yayımlamak | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- publishing web controls
- web controls, publishing
ms.assetid: a7816161-0490-4043-86f5-0f7331ed83b3
caps.latest.revision: 21
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 5238274d66296a21e15b47d1a090ab01c1a1299d
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60046298"
---
# <a name="walkthrough-publishing-a-visual-studio-extension"></a>İzlenecek yol: Visual Studio Uzantısı Yayımlama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

**Not**: Visual Studio Galerisi, Visual Studio Market tarafından değiştirilmektedir. Ayrıntılar için bu konunun en son sürümüne bakın.

Bu izlenecek yol, Visual Studio uzantısı için Visual Studio Galerisine yayımlama gösterilmektedir. Uzantınızı Galerisine eklediğinizde, geliştiriciler kullanabilir **Uzantılar ve güncelleştirmeler** için yeni ve güncelleştirilmiş uzantıları var gidin.

## <a name="prerequisites"></a>Önkoşullar
 Bu izlenecek yolda takip etmek için Visual Studio SDK'yı yüklemeniz gerekir. Daha fazla bilgi için [Visual Studio SDK](../extensibility/visual-studio-sdk.md).

## <a name="create-a-visual-studio-extension"></a>Visual Studio uzantısı oluşturun
 Bu durumda bir varsayılan VSPackage uzantısı kullanacağız, ancak aynı adımları her uzantı türü için geçerlidir.

1. C# ' adlı bir VSPackage'ı oluşturma `TestPublishing` olan bir menü komutu. Daha fazla bilgi için [bir menü komutuyla uzantı oluşturma](../extensibility/creating-an-extension-with-a-menu-command.md).

## <a name="test-the-extension"></a>Uzantıyı test etmek
 Uzantı dağıtmadan önce yapı ve Visual Studio'nun deneysel örneğinde doğru şekilde yüklendiğinden emin olmak için test edin.

1. Visual Studio'da hata ayıklama başlatılamıyor. Visual Studio deneysel örneği açılacak.

2. Deneysel örneğinde Git **Araçları** menüsüne ve ardından **Uzantı Yöneticisi**. TestPublishing uzantısı, Orta bölmede görünür olmalıdır ve etkinleştirilmesi.

3. Üzerinde **Araçları** menüsünde, test komut gördüğünüzden emin olun.

## <a name="publish-the-extension-to-the-visual-studio-gallery"></a>Uzantısı için Visual Studio Galerisine yayımlama
 Artık uzantı Visual Studio Galerisi'nde yayımlayabilirsiniz.

1. Uzantınızı sürümü oluşturulan ve güncel olduğundan emin olun.

2. Bir web tarayıcısında açın [Visual Studio Market](https://marketplace.visualstudio.com/) Web sitesi.

3. Sağ üst köşede **SIGN IN**.

4. Oturum açmak için Microsoft hesabınızı kullanın. Bir Microsoft hesabınız yoksa bir bu noktada oluşturabilirsiniz.

5. **Karşıya Yükle**'ye tıklayın.

6. İçinde **1. adım: Uzantı türü**seçin **aracı** ve ardından **sonraki**.

7. İçinde **2. adım: Karşıya yükleme**, doğrudan Visual Studio Galeri'ye yükleyin ya da yalnızca kendi Web sitesine bir bağlantı eklemek seçebilirsiniz. Bu örnekte **my aracı yüklemek istediğiniz**. **Denetiminizi seçin** kutusu görüntülenir. Tıklayın **Gözat** ve ardından TestPublish.vsix projenin \bin\Release klasörü seçin. **İleri**'ye tıklayın.

8. İçinde **3. adım: Temel bilgileri**, source.extension.vsixmanifest dosyası alanları görüntülenir. Uygun bir seçin **kategori** ve ekleme **etiketleri** uzantınızı bulmalarına yardımcı olmak için. Daha ayrıntılı Özet ve Açıklama (Açıklama 280 en az karakter uzunluğunda olmalıdır) eklemek isteyebilirsiniz. Bırakın **uzantı türü** olarak **Microsoft uzantısı** ve **maliyet kategorisi** olarak **deneme**.

9. Sayfanın alt kısmındaki Katkı Sözleşmesi'ni okuyun ve kontrol **kabul ediyorum**.

10. Tıklayın **katkı oluşturma**. Bu, uzantınızın Visual Studio Galerisi'nde sayfanın henüz yayımlanmadı, bir iletiyle üzerinde olacaktır sayfasını görüntüler.

11. Tıklayın **yayımlama**.

12. Visual Studio Galerisi Uzantınız için arama yapın. Listenin TestPublish uzantısı görüntülenmesi gerekir.

## <a name="install-the-extension-from-the-visual-studio-gallery"></a>Visual Studio Gallery'den uzantıyı yükleme
 Uzantı yayımlandıktan sonra Visual Studio'da yükleyin ve test etmek.

1. Visual Studio'da üzerinde **Araçları** menüsünü tıklatın **Uzantılar ve güncelleştirmeler**.

2. Tıklayın **çevrimiçi** ve sonra TestPublish için arama yapın. Listenin TestPublish uzantısı görüntülenmesi gerekir.

3. **İndir**'e tıklayın. Uzantısı yüklendikten sonra tıklayın **yükleme**.

4. Yüklemeyi tamamlamak için Visual Studio'yu yeniden başlatın.

## <a name="removing-the-extension"></a>Uzantıyı kaldırma
 Uzantı, Visual Studio Galerisi ve bilgisayarınızdan kaldırabilirsiniz.

#### <a name="to-remove-the-extension-from-the-visual-studio-gallery"></a>Visual Studio Gallery'den uzantıyı kaldırmak için

1. Açık [Visual Studio Market](https://marketplace.visualstudio.com/) Web sitesi.

2. Sağ üst köşede **My Extenions**. TestPublish listesi görüntülenir.

3. Tıklayın **Sil**.

#### <a name="to-remove-the-extension-from-your-computer"></a>Uzantıyı bilgisayarınızdan kaldırmak için

1. Visual Studio'da üzerinde **Araçları** menüsünde tıklatın **Uzantı Yöneticisi**.

2. TestPublish seçin ve ardından **kaldırma**.

3. Kaldırma işlemini tamamlamak için Visual Studio'yu yeniden başlatın.
