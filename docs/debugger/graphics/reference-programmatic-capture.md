---
title: Başvuru (programlı yakalama) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: ef60eb8d-1ac2-4e3a-9b4b-f6da0bdd9da8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a462d22df9768d2ffc8b344933e9f5c1f556575a
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56713600"
---
# <a name="reference-programmatic-capture"></a>Başvuru (Programlı Yakalama)
Grafik tanılama yakalama özelliklerini programlı yakalama bir API aracılığıyla programlı denetime destekler. Geçiş ve iletileri grafik tanılama baş üstü (baş yukarı Göster) eklemek, başlatmak ve grafik günlük dosyaları oluşturmak ve grafik bilgilerini yakalamak için bu API'yi kullanabilirsiniz.

## <a name="programmatic-capture-apis"></a>Programlı yakalama API'leri

### <a name="classes"></a>Sınıflar

|Ad|Açıklama|
|----------|-----------------|
|[VsgDbg Sınıfı](vsgdbg-class.md)|Üzerinden grafik tanılama uygulama bileşeninin programlı bir şekilde denetlenen bir arabirimi temsil eder.|

### <a name="preprocessor-symbols"></a>Önişlemci sembolleri

|Ad|Açıklama|
|----------|-----------------|
|[DONT_SAVE_VSGLOG_TO_TEMP](dont-save-vsglog-to-temp.md)|Grafik günlük dosyası, kullanıcı için geçici dosyalar dizini kaydedilip kaydedilmediğini kendi varlığı tanımlar.|
|[VSG_DEFAULT_RUN_FILENAME](vsg-default-run-filename.md)|Grafik günlük dosyası varsayılan dosya adını tanımlar.|
|[VSG_NODEFAULT_INSTANCE](vsg-nodefault-instance.md)|Varsayılan örneği olup olmadığını, varlığı tanımlayan `VsgDbg` sınıfı sağlanır.|

## <a name="related-articles"></a>İlgili Makaleler

| Başlık | Açıklama |
| - | - |
| [Grafik Bilgilerini Yakalama](capturing-graphics-information.md) | Böylece kullanabilirsiniz, DirectX tabanlı uygulamanızdan grafik bilgilerini yakalama gösterir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] işleme sorunlarını tanılamak için grafik tanılama araçları. |
| [Genel bakış](overview-of-visual-studio-graphics-diagnostics.md) | Grafik tanılama DirectX oyunlarındaki ve uygulamalarındaki işleme hatalarını ayıklamanıza nasıl yardımcı olduğu gösterilmektedir. |
