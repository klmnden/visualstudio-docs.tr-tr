---
title: XAML hataları ve Uyarıları
ms.date: 03/06/2018
ms.topic: conceptual
ms.assetid: 34eac8a0-7ec5-4c40-b97a-0126ed367931
author: karann-msft
ms.author: karann
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d3ae795b464d8a693371b1ebb9238a897debbf02
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62892633"
---
# <a name="xaml-errors-and-warnings"></a>XAML hataları ve uyarıları

XAML yazarken, yazdığınız sırada Visual Studio kod analiz eder. Bir hata algılandığında bir dalgalı bir kod satırı görünür. Dalgalı çizgi geldiğinizde, hata veya uyarı hakkında daha fazla bilgi sağlar. Bazı hatalar ve Uyarılar için hızlı eylem ampul görüntülenir ve kullanarak **Ctrl**+**.** klavye kısayolu, sorunu düzeltmek için seçenekleri görüntüler.

## <a name="error-types"></a>Hata türleri

Arka planda birden çok araç, XAML paralel analiz edin. XAML hataları, hatanın algılandığı araca bağlı aşağıdaki üç türlerden birinde ayrılır:

|**Tarafından algılanan hata**|**Hata kodu biçimi**|
| - |-----------------|
|XAML dil hizmeti (XAML Düzenleyicisi)|XLSxxxx|
|XAML Tasarımcısı|XDGxxxx|
|XAML Düzenle ve devam et|XECxxxx|

> [!Note]
> Tüm hata veya uyarı karşılık gelen bir kod vardır. Bu hatalar genellikle XAML Tasarımcısı hatalardır.

## <a name="suppress-xaml-designer-errors"></a>XAML Tasarımcısı Hataları Gizle

Açık **seçenekleri** seçerek iletişim **Araçlar > Seçenekler**ve ardından **metin düzenleyicisi > XAML > çeşitli**.

Onay kutusunu temizleyin **XAML tasarımcısı tarafından algılanan hataları göster** onay kutusu.

![XAML Tasarımcısı Hataları Gizle](../designers/media/suppress_xaml_designer_errors.png)
