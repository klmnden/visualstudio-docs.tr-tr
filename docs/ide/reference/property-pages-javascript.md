---
title: Özellik Sayfaları, JavaScript
ms.date: 06/21/2017
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- javascript.project.property.debugging.debuggertype
- javascript.project.property.debugging.requireauthentication
- javascript.project.property.outputpath
- javascript.project.property.debugging.launchapplication
- javascript.project.property.defaultlanguage
- javascript.project.property.debugging.machinename
- javascript.project.property.debugging.allowlocalnetworkloopback
ms.assetid: a05ab01f-3d5d-4675-a845-eab51807d3a3
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 50b86a32cb055eded71535b84b6b09fd59f78595
ms.sourcegitcommit: ce1ab8a25c66a83e60eab80ed8e1596fe66dd85c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/29/2019
ms.locfileid: "68605942"
---
# <a name="property-pages-javascript"></a>Özellik sayfaları, JavaScript

**Özellik sayfaları** , proje ayarlarına erişim sağlar. Proje özelliklerini değiştirmek için **özellik sayfalarında** görünen sayfaları kullanabilirsiniz.

Proje özelliklerine erişmek için **Çözüm Gezgini**bir proje düğümü seçin. **Proje** menüsünde **Özellikler**' e tıklayın.

[!INCLUDE[note_settings_general](../../data-tools/includes/note_settings_general_md.md)]

Aşağıdaki sayfalar ve Seçenekler **özellik sayfalarında**görünür.

## <a name="configuration-and-platform-page"></a>Yapılandırma ve platform sayfası

Görüntülenecek veya değiştirilecek olan yapılandırmayı ve platformu seçmek için aşağıdaki seçenekleri kullanın.

 **Yapılandırma**

 Görüntülenecek veya değiştirilecek yapılandırma ayarlarını belirtir. Ayarlar **hata ayıklama** (varsayılan), **yayın**, **tüm yapılandırmalar**veya Kullanıcı tanımlı bir yapılandırmadır. Daha fazla bilgi için [nasıl yapılır: Visual Studio](../../debugger/how-to-set-debug-and-release-configurations.md)'da hata ayıklama ve yayın yapılandırmasını ayarlayın.

 **Platformunun**

 Görüntülenecek veya değiştirilecek platform ayarlarını belirtir. Ayarlar **herhangi bir CPU** ( [!INCLUDE[win8_appname_long](../../debugger/includes/win8_appname_long_md.md)] uygulamalar için varsayılan), **x64**, **ARM**, **x86**veya Kullanıcı tanımlı bir platform. Daha fazla bilgi için [nasıl yapılır: Visual Studio](../../debugger/how-to-set-debug-and-release-configurations.md)'da hata ayıklama ve yayın yapılandırmasını ayarlayın.

## <a name="general-page"></a>Genel sayfa

Projenin genel özelliklerini ayarlamak için aşağıdaki seçenekleri kullanın.

> [!NOTE]
> Bazı seçenekler yalnızca UWP uygulamalarında kullanılabilir.

 **Çıkış yolu**

 Projenin yapılandırması için çıkış dosyalarının konumunu belirtir. Yol görelidir; mutlak bir yol girerseniz, mutlak yol projeye kaydedilir. Varsayılan yol bin\Debug.

 Basitleştirilmiş derleme yapılandırması kullandığınızda, proje sistemi bir hata ayıklama veya yayın sürümü oluşturulup oluşturulmayacağını belirler. Hata > ayıklama**başlatma hata ayıklaması** ' ne tıkladığınızda (veya **F5**tuşuna basın), yapı, belirttiğiniz **çıkış yolundan** bağımsız olarak hata ayıklama konumuna konur. Ancak, **Yapı** menüsündeki **Build Solution** komutu onu belirttiğiniz konuma koyar. Gelişmiş derleme yapılandırmalarının etkinleştirilmesi için menü çubuğunda **Araçlar** > **Seçenekler**' i seçin. **Seçenekler** iletişim kutusunda, **Projeler ve çözümler**' i genişletin, **genel**' i seçin ve ardından **Gelişmiş derleme yapılandırmasını göster** onay kutusunu temizleyin. Bu, tüm yapılandırma değerleri üzerinde el ile denetim elde etmenizi ve bir hata ayıklama ya da sürüm sürümünün oluşturulup oluşturulmayacağını sağlar.

 **Varsayılan dil**

 Proje için varsayılan dili belirtir. Denetim Masası 'nda **saat, dil ve bölge** ' de seçilen dil seçeneği kullanıcının tercih ettiği dili belirtir. Proje için varsayılan bir dil belirterek, kullanıcının tercih ettiği dilin uygulamada belirtilen dil kaynaklarıyla eşleşmemesi durumunda belirtilen varsayılan dil kaynaklarının kullanıldığından emin olursunuz.

## <a name="debug-page"></a>Hata ayıklama sayfası

Projedeki hata ayıklama davranışının özelliklerini ayarlamak için aşağıdaki seçenekleri kullanın.

> [!NOTE]
> Bazı seçenekler yalnızca UWP uygulamalarında kullanılabilir.

 **Başlatılacak hata ayıklayıcı**

 Hata ayıklayıcı için varsayılan Konağı belirtir.

- Uygulamayı Visual Studio konak bilgisayarında başlatmak için **yerel makine** ' yi seçin. Daha fazla bilgi için bkz. [Yerel makinede uygulamaları çalıştırma](../../debugger/start-a-debugging-session-for-a-store-app-in-visual-studio-vb-csharp-cpp-and-xaml.md).

- Simülatör 'da uygulamayı başlatmak için **simülatör** ' ı seçin. Daha fazla bilgi için bkz. [simülatörde uygulamaları çalıştırma](../../debugger/run-windows-store-apps-in-the-simulator.md).

- Uzak bir bilgisayarda uygulamayı başlatmak için **uzak makine** ' yi seçin. Uzaktan hata ayıklama hakkında daha fazla bilgi için bkz. [uzak makinede uygulamaları çalıştırma](../../debugger/run-windows-store-apps-on-a-remote-machine.md).

**Uygulamayı Başlat**

**F5** tuşuna bastığınızda uygulamanın başlatılıp başlatılmayacağını belirtir veya **hata** > ayıklama**başlatma hata**Ayıkla ' ya tıklayın. Uygulamayı başlatmak için **Evet** ' i seçin; Aksi takdirde **Hayır**' ı seçin. **Hayır**' ı seçerseniz, uygulamayı başlatmak için farklı bir yöntem kullanıyorsanız uygulamada hata ayıklamaya devam edebilirsiniz.

**Hata ayıklayıcı türü**

Hata ayıklaması yapılacak kod türlerini belirtir. JavaScript kodunda hata ayıklamak için **yalnızca betiği** seçin. Yalnızca ortak dil çalışma zamanı tarafından yönetilen kodda hata ayıklama için **yönetilen** ' ı seçin. **Yalnızca** hata ayıklama C++ kodunda yerel ' i seçin. Hata ayıklama C++ ve JavaScript için **betiği ile yerel** ' i seçin. Hem yönetilen hem de C++ kodun hatalarını ayıklamak için **karışık (yönetilen ve yerel)** seçeneğini belirleyin.

**Yerel ağ geri döngüsüne izin ver**

Uygulama testi için IP geri döngü adresine erişime izin verilip verilmeyeceğini belirtir. İstemci uygulaması, sunucu uygulamasının çalıştığı makinada ise geri döngü adresinin kullanılmasına izin vermek için **Evet** ' i seçin; Aksi takdirde **Hayır**' ı seçin. Bu özellik yalnızca, **başlatma Için hata ayıklayıcı** özelliği **uzak makine**olarak ayarlanırsa kullanılabilir.

**Makine adı**

Hata ayıklayıcıyı barındıracak uzak bilgisayarın adını belirtir. Bu özellik yalnızca **başlatma Için hata ayıklayıcı** **uzak makineye**ayarlanmışsa kullanılabilir.

**Kimlik doğrulaması gerektir**

Uzak bilgisayarın kimlik doğrulaması gerektirip gerektirmediğini belirtir. Bu özellik yalnızca **başlatma Için hata ayıklayıcı** **uzak makineye**ayarlanmışsa kullanılabilir.
