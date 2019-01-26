---
title: Visual Studio komut tablosu (. Vsct) dosyaları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT files, overview
- Visual Studio command table configuration files (VSCT), overview
ms.assetid: 1313adb4-add4-4e74-90e2-f4be522f5259
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: cc265778fcc159a860bda9aa2d7ddafc5342dbd9
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54927314"
---
# <a name="visual-studio-command-table-vsct-files"></a>Visual Studio Komut Tablosu (.Vsct) Dosyaları
Bir komut tablosu yapılandırma dosyası içeren bir VSPackage'ı komut kümesini tanımlayan bir metin dosyasıdır. [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Komut tablosu (VSCT) derleyici XML tabanlı yapılandırma dosyalarını (.vsct) ikili komut tablosu (.cto) çıktı dosyaları derler. Sonuç .cto dosyaları .ctc yapılandırma dosyalarını derlemek için komut tablosu (CTC) derleyiciyi kullanarak oluşturulan aynıdır. Ancak, XML tabanlı .vsct dosyaları, bir XML Düzenleyicisi'ni ve XML IntelliSense'i gibi bazı avantajları vardır.  
  
 .Vsct dosyaları semantiği ve söz dizimi hakkında daha fazla bilgi için bkz: [tasarlama XML komut tablosu (. Vsct) dosyaları](../../extensibility/internals/designing-xml-command-table-dot-vsct-files.md)  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [XML Komut Tablosu (.Vsct) Dosyaları Tasarlama](../../extensibility/internals/designing-xml-command-table-dot-vsct-files.md)  
 .Vsct dosyaları tasarlanacağını açıklar.  
  
 [Nasıl yapılır: Oluşturma bir. Vsct dosyası](../../extensibility/internals/how-to-create-a-dot-vsct-file.md)  
 .Vsct dosyası oluşturma yöntemleriyle karşılaştırır. El ile yeni bir .vsct dosyası oluşturma işlemi açıklanmaktadır.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [VSCT XML Şeması Başvurusu](../../extensibility/vsct-xml-schema-reference.md)  
 Komut tablosu XML yapılandırma dosyasını her bir bölümünü hakkında ayrıntılar sağlar.  
  
 [Komut tablosu yapılandırma (. Ctc) dosyaları](https://msdn.microsoft.com/library/3413dda1-f372-4669-bcf0-c64d3463842c)  
 Kullanım dışı .ctc dosya biçimi'ne genel bakış sunar.  
  
 [VSPackage’ların Kullanıcı Arabirimi Öğeleri Eklemesi](../../extensibility/internals/how-vspackages-add-user-interface-elements.md)  
 Komut tablosu biçim belirtimi açıklar.  
  
 [VSPackage’lardaki Kaynaklar](../../extensibility/internals/resources-in-vspackages.md)  
 Yönetilen ve yönetilmeyen kaynakları yönetilen Vspackage'larda kullanmayı açıklar.  
  
 [Komutlar, Menüler ve Araç Çubukları](../../extensibility/internals/commands-menus-and-toolbars.md)  
 Menüleri, araç çubukları ve komut birleşik giriş kutuları içeren bir kullanıcı Arabirimi oluşturma açıklanmaktadır.