---
title: Basitleştirilmiş ekleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], custom - simple view embedding
ms.assetid: f1292478-a57d-48ec-8c9e-88a23f04ffe5
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c77c7f19ff677ddbe8339c88ef3ea46953e23b7d
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66332070"
---
# <a name="simplified-embedding"></a>Basitleştirilmiş Ekleme
Basitleştirilmiş ekleme etkin bir düzenleyicide kendi belge görünümü nesnesi (diğer bir deyişle, yapılan bir alt öğesi) için üst öğe olduğunda [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane> arabirimi, kendi penceresini komutları işlemek için uygulanır. Basitleştirilmiş ekleme düzenleyicileri etkin denetimleri barındıramaz. Basitleştirilmiş ekleme ile bir düzenleyici oluşturmak için kullanılan nesneleri aşağıdaki çizimde gösterilmektedir.

 ![Basitleştirilmiş ekleme Düzenleyici grafiği](../extensibility/media/vssimplifiedembeddingeditor.gif "vsSimplifiedEmbeddingEditor") Düzenleyicisi ile Basitleştirilmiş ekleme

> [!NOTE]
> Bu çizimde, yalnızca nesnelerin `CYourEditorFactory` nesnesi, standart dosya tabanlı düzenleyici oluşturmak için gereklidir. Özel bir düzenleyici oluşturuyorsanız, uygulama gerekmez <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData2>, düzenleyiciniz olasılıkla kendi özel Kalıcılık mekanizması vardır. Özel olmayan düzenleyiciler için ancak bunu yapmanız gerekir.

 Basitleştirilmiş ekleme ile bir düzenleyici oluşturmak için uygulanan tüm arabirimleri bulunan `CYourEditorDocument` nesne. Ancak, birden çok belge veri görünümleri desteklemek için ayrı veri ve görünüm nesnelere arabirimleri aşağıdaki tabloda gösterildiği gibi bölün.

|Arabirim|Arabirimi konumu|Bir yönetim grubuna bağlanmak veya bağlı bir yönetim grubunun özelliklerini düzenlemek için Yönetim çalışma alanında|
|---------------|---------------------------|---------|
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane>|Görüntüle|Üst pencere bağlantı sağlar.|
|<xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget>|Görüntüle|Komutları işler.|
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser>|Görüntüle|Durum çubuğu güncelleştirmeleri sağlar.|
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsToolboxUser>|Görüntüle|Sağlar **araç kutusu** öğeleri.|
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsFileChangeEvents>|Veri|Dosya değiştiğinde bildirim gönderir.|
|<xref:Microsoft.VisualStudio.Shell.Interop.IPersistFileFormat>|Veri|Bir dosya türü için Farklı Kaydet özelliği sağlar.|
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData2>|Veri|Belge için kalıcılığını etkinleştirir.|
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsDocDataFileChangeControl>|Veri|Dosya değişikliği olayları yeniden tetikleme gibi gizlemeden sağlar.|