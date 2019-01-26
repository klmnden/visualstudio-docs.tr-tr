---
title: Sihirbazı (. Vsz) dosyası | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- .vsz files
- vsz files
- wizards, files
ms.assetid: 72e1d0f3-eef1-455e-b803-96827f030f50
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b1bd68e9d647f9a44eaa8b975995f2d7de3d9640
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55014022"
---
# <a name="wizard-vsz-file"></a>Sihirbaz (.Vsz) Dosyası

Tümleşik geliştirme ortamı (IDE), sihirbazları başlatmak için .vsz dosyalarını kullanır. Bu .vsz dosyaları IDE çağırmak için hangi Sihirbazı belirlemek için kullandığı bilgileri ve sihirbaz için geçirmek için hangi bilgileri içerir.

.Vsz dosyası, bölüm olan bir .ini biçimli metin dosyası sürümüdür. IDE bilinen bilgileri dosyasının başında depolanır. Bu, IDE çağıran sihirbazın .vsz dosyasındaki IDE'ye geçirilecek parametreler arasında bir bağlantı sağlar. Dosyayı geri kalanını sihirbaza özeldir ve IDE tarafından toplanacak olan ve belirli sihirbazın geçirilen parametreleri sağlar.

Aşağıdaki örnek, bir .vsz dosyasının içeriğini gösterir.

```
VSWizard 8.0
Wizard=VsWizard.CBlankSiteWizard -or- {123-1234556-123334}
Param="WIZARDNAME = Wizard One"
Param="WIZARDUI = FALSE"
```

.Vsz dosyası bölümleri aşağıda verilmiştir.

|Bölümü|Açıklama|
|----------|-----------------|
|VSWizard|Dosyadaki ilk parametre, şablon dosyası biçiminin sürüm numarasıdır. Bu sürüm numarası 6.0, 7.0, 7.1 veya 8.0 olmalıdır. Diğer sayılar başlatılamıyor ve biçimi geçersiz hataya neden.|
|Sihirbazı|Bu alan, OLE ProgID Sihirbazı'nın veya alternatif olarak bir CLSID IDE tarafından cocreated Sihirbazı GUID dize gösterimini içerir.|
|param|Bu bölümleri isteğe bağlıdır. Kadar gerekli ekleyebilirsiniz.|

Parametreleri sihirbaza ek özel parametreleri geçirmek üzere .vsz dosyasını olanak tanır. Her değer çeşitleri bir dizide dize öğesi olarak sihirbaza geçirilir. Daha fazla bilgi için [özel parametreler](../../extensibility/internals/custom-parameters.md).

Varsayılan yerel ayar kimliği .vsz dosyanıza eklemek için belirtin `FALLBACK_LCID`xxxx olmak üzere yerel ayar kimliği, örneğin, İngilizce için 1033 xxxx, =. Zaman `FALLBACK_LCID` parametresi tanımlı, geçerli kimlik bulunmazsa sihirbaz sağlanan geri dönüş yerel ayar Kimliğini kullanır.

## <a name="see-also"></a>Ayrıca bkz.

- [Özel Parametreler](../../extensibility/internals/custom-parameters.md)
- [Sihirbazlar](../../extensibility/internals/wizards.md)
- [Şablon Dizin Açıklaması (.Vsdir) Dosyaları](../../extensibility/internals/template-directory-description-dot-vsdir-files.md)