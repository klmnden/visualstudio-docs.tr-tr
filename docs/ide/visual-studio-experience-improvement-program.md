---
title: Müşteri Deneyimi Geliştirme Programı
description: Visual Studio'da gizlilik ayarlarının nasıl yönetileceğini öğrenin.
ms.date: 05/21/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: PoulChapman
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 74ef70228979d1d302a644cda022d086e710b7c7
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54921026"
---
# <a name="visual-studio-customer-experience-improvement-program"></a>Visual Studio Müşteri Deneyimi Geliştirme Programı

Visual Studio Müşteri Deneyimi Geliştirme Programı (VSCEIP), zaman içinde Visual Studio geliştirmesine yardımcı olmak için tasarlanmıştır. Bu program [hatalar hakkında bilgi toplar](../ide/diagnostic-data-collection.md), bilgisayar donanımı ve nasıl kullanıcıların bilgisayardaki görevlerini kesintiye uğratmadan kişiler Visual Studio kullanın. Toplanan bilgiler, Microsoft'un hangi özellikleri belirlemesine yardımcı olur. Bu belgenin içine veya dışına VSCEIP nasıl ele alınmaktadır.

[!INCLUDE [gdpr-hybrid-note](../misc/includes/gdpr-hybrid-note.md)]

## <a name="opt-in-or-out"></a>Veya iyileştirilmiş

VSCEIP varsayılan olarak etkinleştirilir. Kapatın veya yeniden, bu yönergeleri izleyerek yedekleme:

1. Visual Studio’yu çalıştırın.

1. Gelen **yardımcı** menüsünde **geri bildirim gönder**ve ardından **ayarları**.

   **Visual Studio Deneyimini Geliştirme Programı** iletişim kutusu açılır.

1. Geri çevirmek için seçin **Hayır, katılmak istemiyorum**ve ardından **Tamam**.
   Katılım için seçin **Evet, katılmak istiyorum**ve ardından **Tamam**.

   ![Visual Studio Deneyimini Geliştirme Programı iletişim](media/experience-improvement-program.png)

### <a name="registry-settings"></a>Kayıt defteri ayarları

Yüklerseniz [Visual Studio derleme Araçları](https://visualstudio.microsoft.com/downloads/#build-tools-for-visual-studio-2017), VSCEIP yapılandırmak için kayıt defterini güncelleştirmeniz gerekir. Kurumsal müşteriler, kayıt defteri tabanlı bir ilke ayarlayarak içine veya dışına VSCEIP kabul etmek için bir Grup İlkesi oluşturabilirsiniz.

İlgili kayıt defteri anahtarı ve ayarları aşağıdaki gibidir:

64-bit işletim sisteminde, anahtar = **HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\VSCommon\15.0\SQM** 32-bit işletim sisteminde, anahtar = **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\VSCommon\15.0\SQM** olduğunda Grup İlkesi olan etkin, anahtar = **HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\VisualStudio\SQM**

Giriş = **OptIn**

Değer (DWORD) =
- **0** alma (VSCEIP Kapat) kabul
- **1** (VSCEIP Aç) kabul

> [!CAUTION]
> Kayıt defterinin hatalı düzenlenmesi sisteminize ciddi şekilde zarar verebilir. Kayıt defterinde değişiklik yapmadan önce, bilgisayarınızdaki tüm değerli verileri yedeklemelisiniz. Ayrıca **bilinen son iyi yapılandırma** el ile yapılan değişiklikler uygulandıktan sonra sorunlarla karşılaşırsanız başlangıç seçeneği.

İşlenen veya aktarılan VSCEIP tarafından toplanan, bilgileri hakkında daha fazla bilgi için bkz [Microsoft gizlilik bildirimi](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio tarafından toplanan tanılama bilgileri](diagnostic-data-collection.md)
* [Bizimle iletişime geçin](../ide/talk-to-us.md)
* [Visual Studio ile ilgili bir sorun bildirme](../ide/how-to-report-a-problem-with-visual-studio-2017.md)
* [Visual Studio Geliştirici topluluğu](https://developercommunity.visualstudio.com/)
* [Microsoft gizlilik bildirimi](https://privacy.microsoft.com/privacystatement)
