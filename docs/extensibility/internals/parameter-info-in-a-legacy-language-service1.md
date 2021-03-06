---
title: Eski dil Service1 parametre bilgilerini | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- language services, method tips
- method tips
- language services, parameter info tooltip
- IVsMethodData interface
- Parameter Info (IntelliSense)
ms.assetid: f367295e-45b6-45d2-9ec8-77481743beef
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 93283854760c4ab8309d3769550beb664c14f41b
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66314639"
---
# <a name="parameter-info-in-a-legacy-language-service"></a>Eski dil hizmetinde parametre bilgisi
Parametre bilgisi IntelliSense araç ipucu, kullanıcılara bir dil yapısı içinde olduğu hakkında ipuçları sağlar.

 Eski dil Hizmetleri bir VSPackage'ı bir parçası olarak uygulanır, ancak dil hizmeti özellikleri uygulamak için daha yeni MEF uzantıları kullanmaktır. Daha fazla bilgi için bkz. [düzenleyiciyi ve dil hizmetlerini genişletme](../../extensibility/extending-the-editor-and-language-services.md).

> [!NOTE]
> Yeni bir düzenleyici API hemen kullanmaya başlamak öneririz. Bu dil hizmetinizin performansını ve yeni düzenleyici özellikleri yararlanmanıza olanak tanır.

## <a name="how-parameter-info-tooltips-work"></a>Parametre bilgisi araç ipuçlarının nasıl çalışır?
 Düzenleyicide bir deyimi yazdığınızda, yazılan deyiminin tanımını içeren küçük bir araç ipucu penceresi VSPackage'ı görüntüler. Örneğin, bir Microsoft Foundation Classes (MFC) ifadeyi yazın (gibi `pMainFrame ->UpdateWindow`) ve parantez tanımını görüntüleme metot ipucu görünür parametreleri listeleme başlamak için bir tuşa basın `UpdateWindow` yöntemi.

 Parametre bilgisi araç ipuçları, genellikle deyim tamamlama ile birlikte kullanılır. Bunlar, parametre veya anahtar sözcüğü ya da yöntem adı biçimlendirilmiş diğer bilgileri diller için en kullanışlıdır.

 Parametre bilgisi araç ipuçları, komut durdurma aracılığıyla dil hizmeti tarafından başlatılır. Kullanıcı karakter komutlarını kesiştirmek için dil hizmeti nesnenizin uygulamalıdır <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> arabirim ve metin görünümünü geçirmek için bir işaretçi, <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> çağırarak uygulaması <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.AddCommandFilter%2A> yönteminde <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView> arabirimi. Komut filtre kodu penceresine yazdığınız komutları durdurur. Parametre bilgileri kullanıcıya göstermek ne zaman bilmek komut bilgilerini izleyin. Deyim tamamlama, hata işaretçileri ve diğerleri için aynı komutu filtresini kullanabilirsiniz.

 Dil hizmeti için dil hizmeti ipuçları sağlayabilir bir anahtar sözcüğü yazın, ardından oluşturur bir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodTipWindow> nesne ve çağrıları <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.UpdateTipWindow%2A> yönteminde <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView> bir ipucu görüntülemek için IDE bildirmek için arabirim. Oluşturma <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodTipWindow> kullanarak nesne `VSLocalCreateInstance` ve coclass'ı belirterek `CLSID_VsMethodTipWindow`. `VsLocalCreateInstance` çağıran üstbilgi dosyası vsdoc.h içinde tanımlanan bir işlev `QueryService` yerel kayıt defteri ve aramalar için `CreateInstance` için bu nesnede `CLSID_VsMethodTipWindow`.

## <a name="providing-a-method-tip"></a>Metot ipucu sağlama
 Metot ipucu sağlamak için çağrı <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodTipWindow.SetMethodData%2A> yönteminde <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodTipWindow> arabirimi, uygulamanıza geçirmeden <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData> arabirimi.

 Olduğunda, <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData> sınıfı çağrıldığında, metotlarını aşağıdaki sırayla çağrılır:

- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData.GetContextStream%2A>

     Geçerli metin arabelleğini konumu ve ilgili verileri uzunluğunu döndürür. Bu araç ipucu penceresinin bu verilerle gizlememeniz değil IDE'ye bildirir.

- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData.GetCurMethod%2A>

     Başlangıçta görüntülenmesini istediğiniz yöntemi (sıfır tabanlı dizini) döndürür. Sıfır döndürürse, örneğin, ardından ilk aşırı yüklenmiş yöntem başlangıçta sunulur.

- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData.GetOverloadCount%2A>

     Geçerli bağlamda geçerli olan aşırı yüklenmiş yöntemler sayısını döndürür. Bu yöntem için 1'den büyük bir değer döndürürse, daha sonra metin görünümünü yukarı ve aşağı okları sizin için görüntüler. Aşağı oka tıkladığınızda, IDE çağırır <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData.NextMethod%2A> yöntemi. Yukarı Oka tıkladığınızda, IDE çağırır <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData.PrevMethod%2A> yöntemi.

- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData.GetMethodText%2A>

     Parametre bilgisi araç ipucu metnini çeşitli çağrılar sırasında oluşturulan <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData.GetMethodText%2A> ve <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData.GetParameterText%2A> yöntemleri.

- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData.GetParameterCount%2A>

     Yönteminde görüntülemek için parametre sayısını döndürür.

- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData.GetParameterText%2A>

     Görüntülenmesini istediğiniz aşırı yükleme ile ilgili bir yöntem numarası dönerseniz, bu yöntem, ardından bir çağrı tarafından çağrılır <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData.UpdateView%2A> yöntemi.

- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData.UpdateView%2A>

     Metot ipucu görüntülendiğinde Düzenleyicisi, dil hizmetinin bildirir. İçinde <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData.UpdateView%2A> yöntemi, aşağıdaki çağrı:

    ```
    <pTxWin> ->UpdateTipWindow(<pTip>, UTW_CONTENTCHANGED | UTW_CONTEXTCHANGED).
    ```

- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData.OnDismiss%2A>

     Bir çağrı alma <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodData.OnDismiss%2A> yöntemi ipucu penceresini kapattığınızda yöntemi.