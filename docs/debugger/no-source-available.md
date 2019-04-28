---
title: Kullanılabilir kaynak yok | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.nosource
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- No Source Code Available for the Current Location dialog box
ms.assetid: ed0732bc-4b8c-490f-adb1-af06869a2a6b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 85d1d1307a119fa23bf7ba015130ab9c7b6f69d5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62905225"
---
# <a name="no-source-available"></a>Kullanılabilir Kaynak Yok
Projenizin kaynak kodunu görüntülemeye çalıştığınız kod içermiyor. Olağan sebep, kaynak kodu olmayan bir modül çift **çağrı yığını penceresinde** veya **iş parçacıkları penceresi**. Hata ayıklamak, devam edebilirsiniz, ancak kaynak penceresinde kesme noktaları ayarlamak ve bu konumdaki diğer eylemleri gerçekleştirmek için kullanamazsınız. Bir kesme noktası ayarlamak ihtiyacınız varsa, **ayrıştırma penceresi** yerine.

 Çözüm özellik sayfaları'nda hata ayıklayıcı kaynakları dosyalarını nerede arar dizinleri değiştirin ve seçili kaynak dosyaları yoksaymak için hata ayıklayıcının işlemi durdurmasını. Bkz: [kaynak dosyaları, ortak özellikler, çözüm özellik sayfaları iletişim kutusu için hata ayıklama](../debugger/debug-source-files-common-properties-solution-property-pages-dialog-box.md).

 **Kaynak kodu bulmak için Gözat** Burada, göz kaynak kodunu bulmak için bir iletişim kutusunu açmak için bu bağlantıya tıklayın.

 **Ayrıştırılmış Kodu Göster** başlatır **ayrıştırma penceresi**.

 **Eksik kaynak dosyaların ayrıştırmasını her zaman göster** görüntülemek için bu seçeneği belirleyin **ayrıştırma penceresi** otomatik olarak kaynak olduğunda kullanılabilir. Bu ayar, ayrıca değiştirilebilir **seçenekleri** iletişim kutusu, **hata ayıklama** kategori **genel** seçerek veya temizleyerek sayfasında, **ayrıştırılmış Kodu Göster, Kaynak kullanılamıyor**.

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Dosyalarda Hata Ayıklama, Ortak Özellikler, Çözüm Özellik Sayfaları İletişim Kutusu](../debugger/debug-source-files-common-properties-solution-property-pages-dialog-box.md)
- [Simge (.pdb) ve Kaynak Dosyaları Belirtme](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)
- [SOS.dll (SOS Hata Ayıklama Uzantısı)](/dotnet/framework/tools/sos-dll-sos-debugging-extension)