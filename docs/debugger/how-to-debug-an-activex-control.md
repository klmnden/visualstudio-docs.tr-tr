---
title: 'Nasıl yapılır: Bir ActiveX denetiminde hata ayıklama | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vc.controls.debug
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- testing [Visual Studio], test containers
- ActiveX control container debugging [Visual Studio]
- debugging ActiveX controls
- data-bound controls, ActiveX
- test container
- containers, specifying for debug sessions
- ActiveX controls, debugging
- testing [Visual Studio], ActiveX controls
ms.assetid: bbc02cf7-a7e6-44fe-99af-87a43e1d7251
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 059dde50a01c1c71545a187043e60a32a9e68309
ms.sourcegitcommit: 38db86369af19e174b0aba59ba1918a5c4fe4a61
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/14/2019
ms.locfileid: "54269689"
---
# <a name="how-to-debug-an-activex-control"></a>Nasıl yapılır: Bir ActiveX denetiminde hata ayıklama

> [!NOTE]
> Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir. Ayarlarınızı değiştirmek için Araçlar menüsünden içeri ve dışarı aktarma ayarları seçin. Daha fazla bilgi için [ayarlarına](../ide/environment-settings.md#reset-settings).

ActiveX denetimi hata ayıklamak için bir kapsayıcı (çalıştırmak denetimi için yürütülebilir) belirtmeniz gerekir.

## <a name="to-specify-a-container-for-the-debug-session"></a>Hata ayıklama oturumu için bir kapsayıcı belirtmek için

1.  Çözüm Gezgini'nde projeyi seçin.

2.  Gelen **görünümü** menüsünde seçin **özellik sayfaları**.

3.  İçinde **proje özellik sayfaları** açık iletişim kutusunu **yapılandırma özellikleri** klasörü ve select **hata ayıklama**.

4.  Altında **hata ayıklama** kategori bulun **komut** özelliği.

5.  Kapsayıcı için yol adı belirtin. Örneğin, C:\Program Files\Internet Explorer\IEXPLORE. EXE.

6.  Internet Explorer kapsayıcısı olarak belirtin ve etkin Desktop uygulamasını kullanıyorsanız, yazın `/new` içinde **komut satırı bağımsız değişkenlerini** kutusu.

7.  **Tamam**'ı tıklatın.

     Bir kapsayıcıda belirtmezseniz **proje özellik sayfaları** iletişim kutusunda belirtebilirsiniz kapsayıcı hatalarını ayıklamaya başladığınızda. Hata ayıklamayı başlatmak için bir yürütme komutu seçtiğinizde [oturumu için yürütülebilir hata ayıklama iletişim kutusu](../debugger/executable-for-debugging-session-dialog-box.md) görünür. İletişim kutusundaki kapsayıcı yol adını belirtin.

## <a name="see-also"></a>Ayrıca Bkz.

- [ActiveX Denetimleri](/cpp/mfc/activex-controls)
- [Test Kapsayıcısı ile Özellikleri ve Olayları Test Etme](/cpp/mfc/testing-properties-and-events-with-test-container)
- [COM ve ActiveX Hata Ayıklaması](../debugger/com-and-activex-debugging.md)
- [Visual Studio’da hata ayıklama](../debugger/index.md)
- [Hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md)