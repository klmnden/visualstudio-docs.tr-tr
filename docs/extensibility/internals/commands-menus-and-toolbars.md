---
title: Komutlar, menüler ve araç çubukları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- menus [Visual Studio SDK], commands
- commands [Visual Studio]
- toolbars [Visual Studio], commands
ms.assetid: 07b4ed90-dbbd-40df-b6c9-8395fd6f2ab6
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: aed5a91a819658fb141abb4301b9b9499ed602c6
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66311156"
---
# <a name="commands-menus-and-toolbars"></a>Komutlar, menüler ve araç çubukları
Menüleri ve araç çubuklarını, VSPackage komutlarında kullanıcıların erişimi olan. Yazdırma, bir görünümü yenileme veya yeni bir dosya oluşturmak gibi görevleri gerçekleştirmek işlevleri komutlardır. Menüleri ve araç çubuklarını komutlarınızı sunmak için uygun grafik yöntemlerdir. Genellikle, ilgili komutları birlikte aynı menü veya araç çubuğunda kümelenir.

- Menüleri, genellikle bir satırda tümleşik geliştirme ortamı (IDE) veya bir araç penceresinin üst kısmındaki kümelenmiş Tek sözcüklü dizeler olarak görüntülenir. Menüler ayrıca sağ tıklama olay sonucu olarak görüntülenir ve bu bağlamda kısayol menüleri olarak adlandırılır. Tıklandığında, menüler, bir veya daha fazla komut görüntülemek için genişletin. Tıklandığında, komutları, görevleri gerçekleştirmek veya ek komutlar içeren alt menüler başlatın. Bazı iyi bilinen menü adları **dosya**, **Düzenle**, **görünümü**, ve **penceresi**. Daha fazla bilgi için [genişletmek menüler ve komutlar](../../extensibility/extending-menus-and-commands.md).

- Araç çubukları, düğmeler ve birleşik giriş kutuları, liste kutuları, metin kutuları ve menü denetleyicisi gibi başka denetimler satırlarını genellikle cihazlardır. Tüm araç çubuğu denetimleri komutları ile ilişkilidir. Araç çubuğu düğmesini tıkladığınızda ilişkilendirilmiş, komut etkin hale gelir. Araç çubuğu düğmeleri, genellikle bir yazıcıya yazdırma komutu gibi temel alınan komutlar öneren simgeleri olur. Bir açılan liste denetiminde listedeki her öğeyi başka bir komut ile ilişkilidir. Araç çubuğu düğmesi denetimi bir tarafı olduğunu ve diğer tarafında tıklandığında ek komutlar görüntüleyen bir aşağı oka olan karma bir menü denetleyicisidir. Daha fazla bilgi için [araç çubuğuna menü denetleyicisi ekleme](../../extensibility/adding-a-menu-controller-to-a-toolbar.md).

- Bir komut oluşturduğunuzda, aynı zamanda bir olay işleyicisi için oluşturmanız gerekir. Olay işleyicisi belirler komutu görünür veya etkin olduğunda, metin değiştirme olanak tanır ve komut uygun şekilde yanıt vermesini sağlar ("etkinleştirildiğinde rotaları"). Çoğu durumda, IDE kullanarak komutları işleyen <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> arabirimi. İçindeki komutlar [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] yerel seçim temel alınarak ve genel seçime göre en dıştaki bağlamı geçmeden en içteki komut bağlamı ile başlayarak, hiyerarşik bir şekilde rota. Ana menüye eklenen komutlar, komut dosyası için hemen kullanılabilir. Daha fazla bilgi için [MenuCommands vs. OleMenuCommands](../../extensibility/menucommands-vs-olemenucommands.md) ve [seçim bağlamı nesneleri](../../extensibility/internals/selection-context-objects.md).

  Yeni menüleri ve araç çubuklarını tanımlamak için bunları Visual Studio komut tablosu içinde açıklamanız gerekir ( *.vsct*) dosyası. Bu dosya, için hangi komutları, araç çubukları ve şablonda seçili düzenleyicileri desteklemek için gerekli öğeler ile birlikte Visual Studio Paket şablon oluşturur. Alternatif olarak, kendi yazabileceğiniz *.vsct* dosya, burada açıklanan XML şeması kullanarak: [VSCT XML Şeması Başvurusu](../../extensibility/vsct-xml-schema-reference.md).

  İle çalışma hakkında daha fazla bilgi için *.vsct* dosyaları görmek [Visual Studio komut tablosu (.vsct) dosyaları](../../extensibility/internals/visual-studio-command-table-dot-vsct-files.md).

  Bu bölümdeki konularda, komutlar, menüler ve araç çubukları Vspackage'larda nasıl çalıştığı açıklanmaktadır.

## <a name="in-this-section"></a>Bu bölümde
- [VSPackage kullanıcı arabirimi öğelerini nasıl eklenir](../../extensibility/internals/how-vspackages-add-user-interface-elements.md)

 Komut tablosu biçim belirtimi ayrıntılı bir açıklaması.

- [Visual Studio komut tablosu (.vsct) dosyaları](../../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)

 Bir XML tabanlı sözdizimi ve derleyicisi komut tablolar için açıklar.

- [Varsayılan komut, Grup ve araç çubuğu yerleştirme](../../extensibility/internals/default-command-group-and-toolbar-placement.md)

 Önceden tanımlanmış komutları, grupları, menüleri ve araç çubukları açıklar.

- [IDE tanımlı komutlar, menüler ve gruplar](../../extensibility/internals/ide-defined-commands-menus-and-groups.md)

 Önceden tanımlanmış menüler, komutlar ve komut grubu tarafından kullanılmak üzere yok belirtir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE.

- [Komut tasarımı](../../extensibility/internals/command-design.md)

 Komutları tasarım açıklanmaktadır.

- [Menü ve araç çubuğu komutlarını en iyi duruma getirme](../../extensibility/internals/optimizing-menu-and-toolbar-commands.md)

 Komutları için yönergeler sağlar.

- [Komutları kullanılabilir yap](../../extensibility/internals/making-commands-available.md)

 Komutları için Visual Studio tarafından kullanılabilmesini açıklanmaktadır.

- [Komutlar ve menüler birlikte çalışma bütünleştirilmiş kodları kullanın](../../extensibility/internals/commands-and-menus-that-use-interop-assemblies.md)

 Birlikte çalışma bütünleştirilmiş kodları kullanan komutlar uygulanacağını açıklar.

## <a name="related-sections"></a>İlgili bölümler
- [Vspackage'larda komut yönlendirme](../../extensibility/internals/command-routing-in-vspackages.md)

 Vspackage'larda komut yönlendirme açıklar.