---
title: Geri alma tasarımcıları için destek sağlama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- designers [Visual Studio SDK], undo support
ms.assetid: 43eb1f14-b129-404a-8806-5bf9b099b67b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 87ddc0e21a3945ed522014b86174a578c04faa2e
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60095652"
---
# <a name="supply-undo-support-to-designers"></a>Tedarik tasarımcılara geri alma desteği

Tasarımcılar, düzenleyiciler gibi genellikle kullanıcılar, bir kod öğesi değiştirirken son değişikliklerini ters çevirebilirsiniz böylece geri alma işlemlerinin desteklemesi gerekir.

Visual Studio'da uygulanan çoğu tasarımcıları "otomatik olarak ortamı tarafından sağlanan destek" geri"vardır.

Tasarımcı için geri alma özelliğini desteklemek için gereken uygulamaları:

- Soyut temel sınıf uygulayarak geri Yönetimi sağlayın. <xref:System.ComponentModel.Design.UndoEngine>

- Kalıcılık sağlar ve CodeDOM desteği uygulayarak <xref:System.ComponentModel.Design.Serialization.IDesignerSerializationService> ve <xref:System.ComponentModel.Design.IComponentChangeService> sınıfları.

Tasarımcılar kullanarak yazma hakkında daha fazla bilgi için [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)], bkz: [tasarım zamanı desteğini genişletmek](/previous-versions/37899azc(v=vs.140)).

[!INCLUDE[vsipsdk](../extensibility/includes/vsipsdk_md.md)] Varsayılan geri alma altyapısı tarafından sağlar:

- Sağlama, Yönetim uygulamaları aracılığıyla geri <xref:Microsoft.VisualStudio.Shell.Design.OleUndoEngine> ve <xref:Microsoft.VisualStudio.Shell.Design.OleUndoEngine.UndoUnit> sınıfları.

- Kalıcılığı ve varsayılan aracılığıyla CodeDOM desteği sağlayan <xref:System.ComponentModel.Design.Serialization.CodeDomComponentSerializationService> ve <xref:System.ComponentModel.Design.IComponentChangeService> uygulamaları.

## <a name="obtain-undo-support-automatically"></a>Geri alma desteğinin otomatik olarak Al

Visual Studio'da oluşturulan herhangi bir tasarımcı otomatik ve tam geri desteğine sahip ise, Tasarımcı:

- Kullanan bir <xref:System.Windows.Forms.Control> kullanıcı arabirimi için sınıf tabanlı.

- Standart CodeDOM tabanlı kod oluşturma ve ayrıştırma sistem kod oluşturma ve kalıcılığı için kullanır.

   Visual Studio CodeDOM desteği ile çalışma hakkında daha fazla bilgi için bkz. [dinamik kaynak kodu oluşturma ve derleme](/dotnet/framework/reflection-and-codedom/dynamic-source-code-generation-and-compilation).

## <a name="when-to-use-explicit-designer-undo-support"></a>Zaman açık Tasarımcı geri alma desteği
 Tasarımcılar tarafından sağlanan dışındaki bir görünüm bağdaştırıcısı olarak adlandırılan bir grafik kullanıcı arabirimi kullanıyorlarsa kendi geri yönetim sağlaması gerekir <xref:System.Windows.Forms.Control>.

 Buna örnek olarak bir ürün olan bir grafik tasarımı web tabanlı arabirimi oluşturmak olabilir yerine [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)]-grafik arabirim tabanlı.

 Bu gibi durumlarda, Visual Studio kullanarak bu görünüm bağdaştırıcıyı kaydetmek ihtiyacım var <xref:Microsoft.VisualStudio.Shell.Design.ProvideViewAdapterAttribute>ve açık geri alma yönetimi sağlayın.

 Tasarımcılar gereksinim sağlanan Visual Studio kod oluşturma modeli kullanmazsanız CodeDOM ve Kalıcılık desteği sağlamak <xref:System.CodeDom> ad alanı.

## <a name="undo-support-features-of-the-designer"></a>Tasarımcı desteği özelliklerini al
 Ortamı SDK'sı varsayılan uygulamaları sağlamak için gereken arabirimleri geri kullanmayan tasarımcılar tarafından kullanılabilmesi için destek sağlar <xref:System.Windows.Forms.Control> sınıfların kullanıcı arabirimlerini veya standart bir CodeDOM ve Kalıcılık modeli.

 <xref:Microsoft.VisualStudio.Shell.Design.OleUndoEngine> Sınıf türetilir [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] <xref:System.ComponentModel.Design.UndoEngine> uygulaması kullanarak <xref:Microsoft.VisualStudio.OLE.Interop.IOleUndoManager> sınıfı yönetmek için geri alma işlemleri.

 Visual Studio Tasarımcı geri alma için aşağıdaki özellik sağlar:

- Birden çok tasarımcılar arasında bağlantılı geri alma işlevselliği.

- Bir tasarımcı içinde alt birimleri uygulayarak ebeveynleri ile çalışabilirler <xref:Microsoft.VisualStudio.OLE.Interop.IOleUndoUnit> ve <xref:Microsoft.VisualStudio.OLE.Interop.IOleParentUndoUnit> üzerinde <xref:Microsoft.VisualStudio.Shell.Design.OleUndoEngine.UndoUnit>.

Ortamı SDK'sı CodeDOM ve Kalıcılık sağlanarak destek sağlar:

- <xref:System.ComponentModel.Design.Serialization.CodeDomComponentSerializationService> uygulaması olarak <xref:System.ComponentModel.Design.Serialization.IDesignerSerializationService>

- A <xref:System.ComponentModel.Design.IComponentChangeService> Visual Studio tasarım ana bilgisayar tarafından sağlanan.

## <a name="use-the-environment-sdk-features-to-supply-undo-support"></a>Geri alma desteği sağlamak için ortamı SDK Özellikleri'ni kullanın

Geri alma desteği elde etmek için bir tasarımcı uygulayan bir nesne örneği oluşturmalı ve bir örneğini başlatır <xref:Microsoft.VisualStudio.Shell.Design.OleUndoEngine> geçerli bir sınıfla <xref:System.IServiceProvider> uygulaması. Bu <xref:System.IServiceProvider> sınıfı aşağıdaki hizmetleri sağlar:

- <xref:System.ComponentModel.Design.IDesignerHost>.

- <xref:System.ComponentModel.Design.Serialization.IDesignerSerializationService>

   Visual Studio CodeDOM serileştirme kullanarak tasarımcıları kullanmayı seçebilir <xref:System.ComponentModel.Design.Serialization.CodeDomComponentSerializationService> ile sağlanan [!INCLUDE[vsipsdk](../extensibility/includes/vsipsdk_md.md)] uygulaması olarak <xref:System.ComponentModel.Design.Serialization.IDesignerSerializationService>.

   Bu durumda, <xref:System.IServiceProvider> sınıfı için sağlanan <xref:Microsoft.VisualStudio.Shell.Design.OleUndoEngine> Oluşturucusu uygulaması bu nesne döndürmelidir <xref:System.ComponentModel.Design.Serialization.IDesignerSerializationService> sınıfı.

- <xref:System.ComponentModel.Design.IComponentChangeService>

   Varsayılan değeri kullanmanın tasarımcıları <xref:System.ComponentModel.Design.DesignSurface> varsayılan bir uygulama sağlamak için Visual Studio tasarım gereği konak garanti edilir sağlanan <xref:System.ComponentModel.Design.IComponentChangeService> sınıfı.

Uygulama tasarımcıları bir <xref:Microsoft.VisualStudio.Shell.Design.OleUndoEngine> tabanlı geri alma mekanizması, değişiklikleri otomatik olarak izler:

- Özellik değişiklikleri aracılığıyla yapılan <xref:System.ComponentModel.TypeDescriptor> nesne.

- <xref:System.ComponentModel.Design.IComponentChangeService> kabul edilen geri alınamaz bir değişiklik olduğunda olayları el ile oluşturulur.

- Tasarımcı değişikliği bağlamı içinde oluşturulmuş bir <xref:System.ComponentModel.Design.DesignerTransaction>.

- Açıkça kullanarak geri alma birimi uygulaması tarafından sağlanan standart geri alma birimi oluşturmak Tasarımcı seçer <xref:System.ComponentModel.Design.UndoEngine.UndoUnit> veya Visual Studio özel uygulama <xref:Microsoft.VisualStudio.Shell.Design.OleUndoEngine.UndoUnit>, öğesinden türetildiğini <xref:System.ComponentModel.Design.UndoEngine.UndoUnit> ve aynı zamanda sağlayan bir Her iki uygulama <xref:Microsoft.VisualStudio.OLE.Interop.IOleUndoUnit> ve <xref:Microsoft.VisualStudio.OLE.Interop.IOleParentUndoUnit>.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.ComponentModel.Design.UndoEngine>
- <xref:Microsoft.VisualStudio.Shell.Design.OleUndoEngine>
- [Tasarım zamanı desteğini genişletmek](/previous-versions/37899azc(v=vs.140))