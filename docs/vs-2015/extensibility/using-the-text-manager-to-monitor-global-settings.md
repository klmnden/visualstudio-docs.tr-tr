---
title: Genel ayarlar izlemek için metin Yöneticisi'ni kullanarak | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - monitor global settings
- editors [Visual Studio SDK], legacy - text manager
ms.assetid: 023e7671-cf65-419c-9bc1-3c4ee92aa436
caps.latest.revision: 15
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 792c566eda53cb8a4703e8ab03982952c518d8e4
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54763785"
---
# <a name="using-the-text-manager-to-monitor-global-settings"></a>Genel ayarlar izlemek için metin Yöneticisi'ni kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Çekirdek Düzenleyici uygularsanız, bu değişiklikleri örneğinizin düzenleyicisinin etkileyebileceğinden genel ayarlara yapılan değişiklikleri izlemeniz gerekir. Metin Yöneticisi tarafından oluşturulan olaylara dinleyerek değişikliklerini izleyebilirsiniz. Örneğin, çekirdek düzenleyicisinde, kendi belge veri nesnesi gibi bir genel görünümünü veya davranışını bir bileşenin tercih belirttiğinizde metin Yöneticisi bu bilgileri depolar ve tüm etkilenen istemcileri ile iletişim kurar.  
  
## <a name="text-manager-functions"></a>Metin Yöneticisi işlevleri  
 Ayar, aşağıdakiler dahil olmak üzere olayları metin Yöneticisi'ni başlatır:  
  
- Arabellek kaynak kodu denetiminde olup  
  
- Dosya değişikliği bildirimleri için kaydetme  
  
- Görünümleri belirli arabellek ile ilişkili takip etme  
  
- Metin renklendirmesi tercihleri  
  
- Sekme boşluk tercihleri  
  
  Verilen bir dile özgü tercihleri metin Yöneticisi tarafından yönetilmez. Bu ayarlar, her dil hizmeti tarafından yönetiliyor olması gerekir.  
  
  Olay bildirimi için metin Yöneticisi tarafından sağlanır <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextManagerEvents> arabirimi. Bu arabirimi uygulayan istemciniz üzerindeki metin Yöneticisi olaylarını işlemek için nesne oluşturulur. Bu olayları kullanarak kaydetme <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPointContainer> metin manager arabirimi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Çekirdek Düzenleyicisi içinde](../extensibility/inside-the-core-editor.md)   
 [Düzenleyici Özellikleri](http://msdn.microsoft.com/bdac940d-1f14-4019-a01f-fd0bb3dc7198)
