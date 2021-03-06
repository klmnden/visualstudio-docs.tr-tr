---
title: Bir UWP uygulamasında yenileme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- JavaScript debugging, refreshing pages [UWP apps]
- debugging, refreshing pages [UWP apps]
- DOM Explorer, Refresh [UWP apps]
- Refresh [UWP apps]
ms.assetid: fd99ee60-fa94-46df-8b17-369f60bfd908
author: mikejo5000
ms.author: mikejo
manager: jillfra
monikerRange: vs-2017
ms.workload:
- uwp
ms.openlocfilehash: 0ee4c97c4ecbf665bbaef39b658a4b96715acb23
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63408637"
---
# <a name="refresh-a-uwp-app-in-visual-studio"></a>Visual Studio'da bir UWP uygulaması Yenile

 Hata ayıklama ve ardından seçerek JavaScript kullanarak UWP uygulaması yenileme sırasında kodunuzda değişiklikler yapabilirsiniz **Yenile Windows uygulama** düğmesini **hata ayıklama** araç çubuğu. Bu düğmeyi seçerek uygulama hata ayıklayıcıyı durdurup yeniden olmadan yeniden yükler. Yenileme özelliği, HTML, CSS ve JavaScript kodu Değiştir ve hızlı bir şekilde sonuçları görmek sağlar. Bu özellik, UWP uygulamaları için desteklenir.

 Yenileme değil, uygulama durumunu korumak veya uygulamanız için aşağıdaki değişiklikleri yansıtacak:

- Görüntü paketi bildiriminde belirtilen değişiklikler de dahil olmak üzere paket bildirim dosyası değişiklikler.

- Başvuru ekleme veya bir SDK başvurusu kaldırma gibi değiştirir veya Windows çalışma zamanı bileşenleri (.winmd dosyaları) değiştirir.

- Kaynak dizeleri .resjson dosyalardaki değişiklikler gibi değiştirir.

- Proje dosyası yolu adı değişiklikleri, yeni proje dosyaları ya da silinen dosyaları ile sonuçlanan değiştirir.

- Proje ve öğe özellik değişiklikleri seçili hata ayıklama cihazı değişiklikleri gibi veya paket eylemi (Özellikler penceresinde) bir dosya için değişiklikler.

> [!IMPORTANT]
> Başvuruları değiştirme, paket bildirimini değiştirmek veya önceki listesinde belirtilen diğer değişiklikleri yapın, HTML, CSS ve JavaScript kaynak dosyalarını güncelleştirmek için hata ayıklayıcıyı yeniden başlatın ve durdurun gerekir.

### <a name="to-refresh-an-app"></a>Bir uygulamayı yenilemek için

1. Visual Studio'da açın, UWP projesi ile seçin **yerel makine** hata ayıklama hedefi olarak.

     ![Select hata ayıklama hedef liste](../debugger/media/js_select_target.png "JS_Select_Target")

3. Uygulamayı hata ayıklama modunda çalıştırmak için F5 tuşuna basın.

4. Visual Studio'ya geçiş yapın.

5. UWP uygulamanızın giriş sayfasının HTML bazıları düzenleyin.

7. Tıklayın **Yenile Windows uygulama** şuna benzeyen düğmesi: ![Windows uygulama düğmesine Yenile](../debugger/media/js_refresh.png "JS_Refresh"). (Veya F4 tuşuna basın.)

8. Uygulamasına geçin. Uygulama yüklenir ve güncelleştirilmiş HTML uygulaması oluşturmak için kullanılır.

## <a name="see-also"></a>Ayrıca Bkz.
- [Hızlı Başlangıç: HTML ve CSS hatalarını ayıklama](../debugger/quickstart-debug-html-and-css.md)