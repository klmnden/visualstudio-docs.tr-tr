---
title: Görünüm hata ayıklayıcıda değerleri kaydetme | Microsoft Docs
ms.custom: seodec18
ms.date: 11/19/2018
ms.topic: conceptual
f1_keywords:
- vs.debug.registers
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- registers, debugging
- register contents
- flags, Registers window
- register groups
- debugging [Visual Studio], Registers window
- Registers window
ms.assetid: 2918ffa2-562f-40d6-9053-ef321bbeb767
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: afcada407060af2072e3cf1c30e86153762890b5
ms.sourcegitcommit: 847d192013eb8225776243045c9b5a53d1ba4a59
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/15/2019
ms.locfileid: "59584395"
---
# <a name="view-register-values-in-the-registers-window-c-c-visual-basic-f"></a>Görüntüleme değerleri yazmaçlar penceresi içinde kaydetmek (C#, C++, Visual Basic F#)

**Kaydeder** penceresi görüntülendiğinde, Visual Studio hata ayıklama sırasında içeriklerini kaydedin. Yazmaçları kavramları üst düzey bir giriş için ve **kaydeder** penceresinde görmek [hata ayıklama temelleri: Yazmaçlar penceresi](../debugger/debugging-basics-registers-window.md).

> [!NOTE]
> Betik veya SQL uygulamalar için kayıt bilgileri kullanılamıyor.

Uygulamanızda kodu yürütür olarak hata ayıklama sırasında değişiklik değerleri kaydedin. Değişen değerler kısa bir süre önce görünür kırmızıyla **kaydeder** penceresi.

Dağınıklığı, azaltmak için **kaydeder** penceresi kayıtları platform ve işlemci göre değişiklik gösteren gruplar halinde düzenler türü. Görüntüleyebilir ya da yazmaç gruplarını gizleyebilirsiniz. Daha fazla bilgi için [nasıl yapılır: Görüntüleme ve gizleme yazmaç gruplarını](../debugger/how-to-display-and-hide-register-groups.md).

Bayraklar hakkında daha fazla bilgi için bkz **kaydeder** penceresinde görmek [penceresi hakkında kaydeder](../debugger/debugging-basics-registers-window.md)

YAZMAÇ değerlerini düzenleyebilirsiniz. Daha fazla bilgi için [nasıl yapılır: YAZMAÇ değerini düzenleme](../debugger/how-to-edit-a-register-value.md).

**Yazmaçlar penceresi açmak için**

1. Adres seviyesinde, seçerek hata ayıklamayı **adres seviyesinde hata ayıklamayı** içinde **Araçları** (veya **hata ayıklama**) > **seçenekleri**  >  **Hata ayıklama**.

1. Hata ayıklama kesme noktası veya çalışıyor olsa da seçin **hata ayıklama** > **Windows** > **kaydeder**, veya basın **Alt** + **5**.

>[!NOTE]
>İletişim kutuları ve menü komutları, Visual Studio sürümü veya ayarlarınızı bağlı olarak farklı olabilir. Ayarlarınızı değiştirmek için seçin **içeri ve dışarı aktarma ayarları** Visual Studio **Araçları** menüsü. Daha fazla bilgi için [ayarlarına](../ide/environment-settings.md#reset-settings).

### <a name="see-also"></a>Ayrıca bkz.

- [Hata ayıklama temelleri: Yazmaçlar penceresi](../debugger/debugging-basics-registers-window.md)
- [Hata ayıklayıcıda verileri görüntüleme](../debugger/viewing-data-in-the-debugger.md)
