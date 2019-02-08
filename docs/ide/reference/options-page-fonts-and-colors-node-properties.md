---
title: Seçenekler Sayfası, Yazı Tipleri ve Renkler Düğümü Özellikleri
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- Tools Options settings, Fonts and Colors node properties
- automation [Visual Studio], controlling Tools Options
ms.assetid: 8e1ab784-5f85-4e2b-8ef9-e5d59ca4dbcb
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b5363d71082128c13146c445fe312424be7e4340
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55907367"
---
# <a name="options-page-fonts-and-colors-node-properties"></a>Seçenekler Sayfası, Yazı Tipleri ve Renkler Düğümü Özellikleri
Bu belgede, altında görünmesi için kayıtlı bir araç penceresi için yazı tipi ve renk özellikleri açıklanmaktadır. **yazı tipleri ve renkler** içinde **ortam** kategorisi **seçenekleri** iletişim kutusu. Bu, dinamik doğasını VSPackages yüklenmediyse veya değiştirebilirsiniz renklendirilebilir öğeleri gruplarını destekler.

 Aşağıdaki bölümde, örnek bir kayıtlı penceresi türü ve her bir pencere için kullanılabilir olan özellikleri gösterir.

## <a name="text-editor-or-printer-or-dialogs-and-tool-windows"></a>Metin düzenleyici veya yazıcı veya iletişim kutuları ve araç Windows
 `DTE.Properties("FontsAndColors", "TextEditor")`

 -veya-

 `DTE.Properties("FontsAndColors", "Printer")`

 -veya-

 `DTE.Properties("FontsAndColors", "Dialogs and Tool Windows")`

|Özellik Öğesi Adı|Değer|Açıklama|
| - |-----------|-----------------|
|FontFamily|Get/Set (dize)|"Courier gibi yeni." kullanılacak yazı tipi adı|
|FontCharacterSet|Get/Set (<xref:EnvDTE.vsFontCharSet>)|A <xref:EnvDTE.vsFontCharSet> İbranice veya Rusça gibi kullanmak için karakter türünü belirten bir değer.|
|FontSize|Get/Set (kısa)|Noktaları kullanılacak yazı tipi boyutu. Örneğin, 10 veya 12.|

## <a name="see-also"></a>Ayrıca Bkz.

- [Seçenek ayarlarını denetleme](https://msdn.microsoft.com/Library/a09ed242-7494-4cde-bbd1-7a8ec617965d)
- [Seçenekler sayfasında özellik öğelerinin adlarını belirleme](https://msdn.microsoft.com/Library/d450422d-47c7-4eeb-9f9f-3286264bc5aa)
- [Seçenekler Sayfası, Ortam Düğümü Özellikleri](../../ide/reference/options-page-environment-node-properties.md)
- [Seçenekler Sayfası, Metin Düzenleyici Düğümü Özellikleri](../../ide/reference/options-page-text-editor-node-properties.md)