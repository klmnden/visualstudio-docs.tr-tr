---
title: 'Nasıl yapılır: Metin işaretçileri kullanma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - using text markers
ms.assetid: 76eed51c-eecb-4579-823e-13df2f0526b9
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 25c3c4f3a3d9a253b9ec671892d0d44ccf9ca3ab
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63430955"
---
# <a name="how-to-use-text-markers"></a>Nasıl yapılır: Metin işaretçileri kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Düzenlemek için metin işaretçileri uygulanabilir bir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer> nesne.  
  
## <a name="procedures"></a>Yordamlar  
  
#### <a name="to-apply-text-markers"></a>Metin işaretçileri uygulamak için  
  
1. Bir örneği elde <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextManager> sınıfı.  
  
    > [!NOTE]
    > Çekirdek Düzenleyici düzenlemekte olduğu herhangi bir belge otomatik olarak standart metin işaretçileri uygular ve standart metin işaretçileri açıkça uygulamak gerekli olmamalıdır.  
  
2. İşaret türü kimliği, ilgilendiğiniz çağırarak işaretinin elde <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextManager.GetRegisteredMarkerTypeID%2A> yöntemiyle `GUID` , çalışmak istediğiniz metin işaretçisi.  
  
    > [!NOTE]
    > Kullanmayın `GUID` VSPackage'ı veya metin işaretçisi sağlayan hizmet.  
  
3. İşaret türü kimliği elde çağırarak kullanım <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextManager.GetRegisteredMarkerTypeID%2A> yöntemi çağırmak için bir parametre olarak <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines.CreateLineMarker%2A> yöntemi veya <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextStream.CreateStreamMarker%2A> metin işaretçisi metnin belirli bir bölgeye uygulamak için yöntemi.  
  
#### <a name="to-add-features-to-text-markers"></a>Metin işaretçileri için özellikler eklemek için  
  
1. Bir metin işaretçisi araç ipuçları, özel bağlam menüsü veya işleyici gibi özel durumlar için ek özellikler eklemek için istenebilir. Bunu yapmak için:  
  
2. Bir nesneyi uygulama oluşturma <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextMarkerClient> arabirimi.  
  
3. Ek işlevler isterseniz, uygulama <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextMarkerClientEx>ve <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextMarkerClientAdvanced> arabirimleri uygulayan aynı nesne üzerinde <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextMarkerClient> arabirimi.  
  
4. Geçirmek <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextMarkerClient> çağrısına oluşturma arabirimi <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines.CreateLineMarker%2A> yöntemi veya <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextStream.CreateStreamMarker%2A> metin işaretçisi metnin belirli bir bölgeye uygulamak için kullanılan yöntem.  
  
5. Bağlam menüsü destek bir metin işaretçisi bölgeye eklerken menü oluşturmak gereklidir.  
  
     Bir bağlam menüsü bakın oluşturma hakkında daha fazla bilgi için [bağlam menüleri](../extensibility/context-menus.md).  
  
6. [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Ortam çağırır sağlanan arabirim yöntemleri gibi <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextMarkerClient.GetTipText%2A> yöntemi veya <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextMarkerClient.ExecMarkerCommand%2A> gerektiğinde yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Metin işaretçileri eski API'si ile kullanma](../extensibility/using-text-markers-with-the-legacy-api.md)   
 [Nasıl yapılır: Standart metin işaretçileri Ekle](../extensibility/how-to-add-standard-text-markers.md)   
 [Nasıl yapılır: Özel metin işaretçileri oluşturma](../extensibility/how-to-create-custom-text-markers.md)   
 [Nasıl yapılır: Hata İşaretçileri Uygulama](../extensibility/how-to-implement-error-markers.md)
