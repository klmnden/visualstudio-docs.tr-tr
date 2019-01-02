---
title: Microsoft Office sistemi projesi için Visual Studio araçlarını açmak veya oluşturmak için VBA erişimi etkinleştirme
decsprition: You must explicitly enable access to the Office VBA project system before you can create or open a Visual Studio Tools for Office system project
titleSuffix: ''
ms.custom: seodec18
ms.date: 02/02/2017
ms.prod: visual-studio-dev15
ms.topic: conceptual
f1_keywords:
- vst.project.vbawrongversion
- VST.Project.VBASecurityGenericError
- VST.Project.VBASecurityPermissions
- VST.SelectDocWizard.MissingCOM
- VST.Project.VBASecurityNotSet
dev_langs:
- VB
- CSharp
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 0404498490569d3c9edee5b9e190535eafcb105b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53933495"
---
# <a name="enable-access-to-vba-to-create-or-open-a-visual-studio-tools-for-the-microsoft-office-system-project"></a>Microsoft Office sistemi projesi için Visual Studio araçlarını açmak veya oluşturmak için VBA erişimi etkinleştirme

Microsoft Office sistemi projesi için Visual Studio araçlarını açmak veya oluşturmak için önce Visual Basic for Applications (VBA) Microsoft Office proje sistemine erişimi açıkça etkinleştirmeniz gerekir.

 Uygulamalar için Visual Basic projeleri kullanmayın olsa da Microsoft Office geliştirme projeleri Applications (VBA) Microsoft Office Word ve Microsoft Office Excel, proje sistemi için Visual Basic erişim gerektirir. Hem Visual Basic denetimleri tasarım zamanı desteği ve C# projeleri, Visual Basic for Applications proje sistemine bağlıdır.

 Visual Basic for Applications proje sistemine kendilerini yayılması bir şekilde otomatik hale getirmek bazı Microsoft Office makro virüslerinin çalışır. Visual Basic for Applications proje sistemine erişimi etkinleştirerek, makro virüslerinin yayılmasını engellemeye yardımcı olan bir koruma'yı kaldırın. Ancak, herhangi bir makronun bilgisayarınızda çalışıp çalışmayacağını makro güvenlik düzeyini ve Office uygulamalarınızı korumak Güvenilen Yayımcılar listesi belirleyecek şekilde normal makro güvenliği yerinde kalır.

> [!NOTE]
> Bu, yalnızca geliştirme bilgisayarında geçerlidir. Son kullanıcı bilgisayarlarında Office çözümlerinin çalışması için etkin. Bu seçenek gerekli değildir.

 Üzerinde Visual Basic for Applications proje sistemine erişimi devre dışı bırakılması kendi, virüslere karşı koruma sağlamaz, yalnızca virüsler bilgisayarınızı sürekli bir makro bulaşır caspol.exe'nin diğer belgelere yayılmasını durdurmaya yardımcı olduğunu dikkate almak önemlidir virüs. Varsayılan olarak, bilgisayar için korumayı, ek bir katmanı olarak seçeneği devre dışıdır, ancak en iyi güvenlik uygulamalarını takip ediyorsanız, etkinleştirme bilgisayarınızda virüsler için daha fazla etkilenmesini yapmaz.

 En iyi korumayı karşı Office makro virüslerinin olduğundan, yalnızca makrolarından güvenecek şekilde yüksek veya çok yüksek güvenlik düzeyinde Office çalıştırmak için bilinen kaynakları doğrulandı ve güvenlik yamaları ve virüs tarayıcıları ile güncel kalın.

 Bilgisayarınızda virüsler ve diğer kötü amaçlı kod koruma hakkında daha fazla bilgi için bkz. [ http://www.microsoft.com/protect ](http://www.microsoft.com/protect).

 Etkinleştirebilir veya devre dışı bırakma seçeneği **Visual Basic projeye erişimi güven** el ile.

 VBA veya COM hatalar görürseniz Office yüklemenizi onarmak için.

## <a name="to-enable-or-disable-access-to-visual-basic-projects"></a>Etkinleştirme veya Visual Basic projelerine erişimi devre dışı

1. Tıklayın **dosya** sekmesi.

2. Tıklayın **seçenekleri**.

3. Tıklayın **Güven Merkezi**ve ardından **Güven Merkezi Ayarları**.

4. İçinde **Güven Merkezi**, tıklayın **makrosu ayarları**.

5. İşaretleyin veya işaretini kaldırın **VBA projesi nesne modeline erişim güven** etkinleştirme veya Visual Basic projelerine erişimi devre dışı.

6. **Tamam**'ı tıklatın.

### <a name="to-enable-or-disable-access-to-visual-basic-projects-with-the-2007-microsoft-office-system"></a>Etkinleştirme veya Visual Basic projeleri 2007 Microsoft Office sistemi ile erişimi devre dışı

1. Üzerinde **Araçları** menü Word veya Excel'de işaret **makrosu**ve ardından **güvenlik**.

2. İçinde **güvenlik** iletişim kutusu, tıklayın **Güvenilen Yayımcılar** sekmesi.

3. Etkinleştirmek veya clear devre dışı bırakmak için seçin **Visual Basic projeye erişimi güven**.

4. **Tamam**'ı tıklatın.

## <a name="to-set-your-office-macro-security-level"></a>Office makro güvenlik düzeyini ayarlamak için

1. Tıklayın **dosya** sekmesi.

2. Tıklayın **seçenekleri**.

3. Tıklayın **Güven Merkezi**ve ardından **Güven Merkezi Ayarları**.

4. İçinde **Güven Merkezi**, tıklayın **makrosu ayarları**.

5. İçinde **makrosu ayarları** bölümünde, istediğiniz ayarı seçin.

6. **Tamam**'ı tıklatın.

### <a name="to-set-your-office-macro-security-level-with-the-2007-microsoft-office-system"></a>2007 Microsoft Office sistemi ile Office makro güvenlik düzeyini ayarlamak için

1. Üzerinde **Araçları** menü Word veya Excel'de işaret **makrosu**ve ardından **güvenlik**.

2. Üzerinde **güvenlik düzeyi** sekmesinde, istediğiniz ayarı seçin.

    **Güvenlik düzeyi** sekmesi, her düzeyi hakkındaki ayrıntıları içerir. Daha fazla bilgi için Office Yardımı'nda "makro güvenlik düzeyleri" konusuna bakın.

### <a name="to-install-vba-with-the-2007-microsoft-office-system"></a>VBA 2007 Microsoft Office sistemi ile yüklemek için

1. Denetim Masası'ndaki çalıştırma **Program Ekle veya Kaldır** veya **programlar ve Özellikler**.

2. Office seçin **şu anda yüklü programlar** listesi.

3. **Değiştir**'i tıklatın.

4. Seçin **Özellik Ekle veya Kaldır**ve ardından **devam**.

5. Seçin **Gelişmiş özelleştirme uygulama Seç**ve ardından **sonraki**.

6. Genişletin **Paylaşılan Office özellikleri** içinde **uygulama ve araçların için güncelleştirme seçeneklerini belirle** listesi.

7. Aşağı açılan menüyü açmak **uygulamalar için Visual Basic**ve ardından **Bilgisayarımdan Çalıştır**.

8. **Devam**'a tıklayın.

9. **Kapat**'ı tıklatın.

## <a name="to-repair-your-installation-of-office"></a>Office yüklemenizi onarmak için

1. Denetim Masası'ndaki çalıştırma **Program Ekle veya Kaldır** veya **programlar ve Özellikler**.

2. Office sürümünüz seçin **şu anda yüklü programlar** listesi.

3. **Değiştir**'i tıklatın.

4. Seçin **yeniden yükleyin veya onarın**ve ardından **sonraki**.

5. Seçin **Office yükleme hatalarını algılama ve onarma**ve ardından **yükleme**.

## <a name="see-also"></a>Ayrıca bkz.

 [Office çözümleri güvenliğini sağlama](../vsto/securing-office-solutions.md)