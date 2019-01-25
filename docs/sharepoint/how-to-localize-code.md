---
title: 'Nasıl yapılır: Kod yerelleştirme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- localizing code [SharePoint development in Visual Studio]
- SharePoint development in Visual Studio, localizing
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 8d61f9f0dff98d25185233fcf07bc937de3a6455
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54862805"
---
# <a name="how-to-localize-code"></a>Nasıl yapılır: Kod yerelleştirme
  Yerelleştirilmemiş kod, sabit kodlanmış dize değerleri kullanır. Kod dizelerini yerelleştirmek için bunları çağrılarıyla değiştirin <xref:System.Web.HttpContext.GetGlobalResourceObject%2A>, yerelleştirilmiş kaynaklara başvuran bir yöntemi.  
  
## <a name="localize-code"></a>Kod yerelleştirme  
  
#### <a name="to-localize-code"></a>Kodu yerelleştirmek için  
  
1.  İçinde **Çözüm Gezgini**, bir proje öğesi için kısayol menüsünü açın ve ardından **Ekle** > **Modülü**.  
  
     Seçin **kaynak dosyası** şablonu.  
  
    > [!NOTE]  
    >  Böylece dağıtım türü özelliğinin kullanılabilir kaynak dosyasını bir SharePoint projesine eklediğinizden emin olun. Bu yordamda daha sonra bu özellik gereklidir.  
  
2.  Varsayılan kaynak dosyasına protokolün kendi tercih ettiğiniz bir ad verin bir *.resx* uzantısı gibi *MyAppResources.resx*.  
  
3.  1. ve 2 SharePoint proje öğesine ayrı kaynak dosyaları eklemek için adımları yineleyin: her bir yerelleştirme dili.  
  
     Her bir yerelleştirilmiş kaynak dosyası için aynı temel adı kullanın, ancak kültür kimliğini ekleyin. Örneğin, kaynak adı Almanca yerelleştirilmiş *MyAppResources.de-DE.resx*.  
  
4.  Her kaynak dosyasını açın ve yerelleştirilmiş dizeleri ekleyin. Her dosyada aynı dize kimliklerini kullanın.  
  
5.  Değiştirin **dağıtım türü** özelliği için her kaynak dosyasının **AppGlobalResource** sunucunun App_GlobalResources klasörüne dağıtılacak her dosya neden olacak.  
  
6.  Değerini değiştirmeden bırakın **derleme eylemi** özelliği her bir dosyanın **gömülü kaynak**.  
  
     Gömülü kaynaklar proje DLL'SİNDE derlenir.  
  
7.  Kaynak uydu DLL'lerini oluşturmak için projeyi derleyin.  
  
8.  İçinde **paket Tasarımcısı**, seçin **Gelişmiş** sekmesine ve ardından uydu derlemesini ekleyin.  
  
9. İçinde **konumu** kutusunda, aşağıdaki gibi bir kültür kimlik klasörünü konum yolunun önüne ekleyin *de-DE\\\<proje öğe adı >. resources.dll*.  
  
10. Çözümünüz System.Web derlemesine önceden başvurmuyorsa buna bir başvuru ekleyin ve kodunuzda bir yönerge ekleyin <xref:System.Web>.  
  
11. UI metni, hatalar ve ileti metni gibi kullanıcılar tarafından görülebilir, kodunuzda sabit kodlanmış tüm dizeleri bulun. Bunları bir çağrısı ile Değiştir <xref:System.Web.HttpContext.GetGlobalResourceObject%2A> yöntemi aşağıdaki sözdizimini kullanarak:  
  
    ```csharp  
    HttpContext.GetGlobalResourceObject("Resource File Name", "String ID")  
    ```  
  
12. Seçin **F5** anahtarı oluşturun ve uygulamayı çalıştırın.  
  
13. SharePoint'te, varsayılan görüntüleme dilini değiştirin.  
  
     Yerelleştirilmiş dizeleri uygulamada görüntülenir. Yerelleştirilmiş kaynakları görüntülemek için SharePoint server kaynak dosyanın kültürüyle eşleşen bir dil paketi yüklü olmalıdır.  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint Çözümlerini Yerelleştirme](../sharepoint/localizing-sharepoint-solutions.md)   
 [Nasıl yapılır: Bir özelliği yerelleştirme](../sharepoint/how-to-localize-a-feature.md)   
 [Nasıl yapılır: ASPX işaretlemesini yerelleştirme](../sharepoint/how-to-localize-aspx-markup.md)   
 [Nasıl yapılır: Kaynak dosyası ekleme](../sharepoint/how-to-add-a-resource-file.md)  
