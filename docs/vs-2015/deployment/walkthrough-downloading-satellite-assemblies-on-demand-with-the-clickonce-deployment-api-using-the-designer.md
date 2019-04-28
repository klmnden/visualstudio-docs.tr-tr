---
title: 'İzlenecek yol: API tasarımcıyı kullanarak ClickOnce dağıtımı ile uydu derlemelerini indirme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- Windows Forms, globalization
- ClickOnce deployment, globalization
- localization, Windows Forms
- ClickOnce, on-demand download
- Windows Forms, localization
- ClickOnce deployment, localization
- walkthroughs, localization
ms.assetid: 82b85a47-b223-4221-a17c-38a52c3fb6e2
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 559fb1f3613b42bd2c972f61b45736b07e76a318
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62420025"
---
# <a name="walkthrough-downloading-satellite-assemblies-on-demand-with-the-clickonce-deployment-api-using-the-designer"></a>İzlenecek yol: API tasarımcıyı kullanarak ClickOnce dağıtımı ile uydu derlemelerini indirme

[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Windows Forms uygulamaları için uydu derlemelerini kullanarak birden çok kültürde yapılandırılabilir. A *uydu derleme* uygulamanın varsayılan kültürünü dışındaki bir kültür için uygulama kaynaklarını içeren bir derlemedir.

Bölümünde açıklandığı gibi [ClickOnce uygulamalarını yerelleştirme](../deployment/localizing-clickonce-applications.md), birden çok uydu derlemeleri aynı birden çok kültürde içerebilir [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] dağıtım. Varsayılan olarak, [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] tek bir istemci, büyük olasılıkla yalnızca bir uydu derlemesine gereksinim duyacak olmanıza rağmen tüm uydu derlemeler, dağıtımınızdaki istemci makineye indirir.

Bu yönerge, uydu derlemeleri isteğe bağlı olarak işaretleme ve istemci makinesi, geçerli kültür ayarları için ihtiyaç duyduğu derlemeyi indirme nasıl gösterir.

> [!NOTE]
> Test amacıyla, aşağıdaki kod örnekleri programlı olarak kültürü kümesine `ja-JP`. Bir üretim ortamı için bu kodu ayarlama konusunda bilgi için bu konunun ilerleyen bölümlerindeki "Sonraki adımlar" bölümüne bakın.

### <a name="to-mark-satellite-assemblies-as-optional"></a>Uydu derlemeleri isteğe bağlı olarak işaretlemek için

1. Projenizi yapılandırın. Bu, tüm kültürler için yerelleştirme için uydu derlemeleri üretir.

2. Çözüm Gezgini'nde proje adına sağ tıklayın ve **özellikleri**.

3. Tıklayın **Yayımla** sekmesine ve ardından **uygulama dosyaları**.

4. Seçin **tüm dosyaları göster** uydu derlemelerini görüntülemek için onay kutusu. Varsayılan olarak tüm uydu derlemelerini, dağıtımınızdaki dahil edilir ve bu iletişim kutusunda görünmez.

     Uydu derlemesi biçiminde bir ada sahip olacaktır *isoCode*\ApplicationName.resources.dll, burada *isoCode* RFC 1766 biçiminde bir dil tanımlayıcısı.

5. Tıklayın **yeni...**  içinde **indirme grubu** listesini her bir dil tanımlayıcısı. İndirme grubu adı için istendiğinde dil tanımlayıcısı girin. Örneğin, Japonca uydu derlemesi için indirme grubu adını belirtirsiniz `ja-JP`.

6. Kapat **uygulama dosyaları** iletişim kutusu.

### <a name="to-download-satellite-assemblies-on-demand-in-c"></a>C'de uydu derlemelerini yüklemek için\#

1. Program.cs dosyasını açın. Bu dosya Çözüm Gezgini'nde, projenizi seçin görmüyorsanız ve üzerinde **proje** menüsünü tıklatın **tüm dosyaları göster**.

2. Uygun bir uydu derlemesini indirmek ve uygulamanızı başlatmak için aşağıdaki kodu kullanın.

     [!code-csharp[ClickOnce.SatelliteAssemblies#1](../snippets/csharp/VS_Snippets_Winforms/ClickOnce.SatelliteAssemblies/CS/Program.cs#1)]

### <a name="to-download-satellite-assemblies-on-demand-in-visual-basic"></a>Visual Basic'te uydu derlemelerini yüklemek için

1. İçinde **özellikleri** uygulamanın pencereye tıklayın **uygulama** sekmesi.

2. Sekme sayfanın en altında tıklayın **uygulama olaylarını görüntüle**.

3. Aşağıdaki içeri aktarmaları ApplicationEvents.VB dosyasının başına ekleyin.

     [!code-vb[ClickOnce.SatelliteAssembliesVB#1](../snippets/visualbasic/VS_Snippets_Winforms/ClickOnce.SatelliteAssembliesVB/VB/ApplicationEvents.vb#1)]

4. Aşağıdaki kodu ekleyin `MyApplication` sınıfı.

     [!code-vb[ClickOnce.SatelliteAssembliesVB#2](../snippets/visualbasic/VS_Snippets_Winforms/ClickOnce.SatelliteAssembliesVB/VB/ApplicationEvents.vb#2)]

## <a name="next-steps"></a>Sonraki Adımlar

Bir üretim ortamında, büyük olasılıkla kod örneklerinde ayarlar şu satırı kaldırın gerekir <xref:System.Threading.Thread.CurrentUICulture%2A> belirli bir değere istemci makinelere doğru değerine ayarlanmış olduğundan varsayılan olarak. Japonca istemci makine üzerinde örneğin, uygulamanız çalıştığında zaman <xref:System.Threading.Thread.CurrentUICulture%2A> olacaktır `ja-JP` varsayılan olarak. Programlı olarak ayarlama, uydu bütünleştirilmiş kodlarınızı Uygulamanızı dağıtmadan önce test etmek için iyi bir yoludur.

## <a name="see-also"></a>Ayrıca Bkz.

- [İzlenecek yol: ClickOnce Dağıtım API'si ile Uydu Derlemelerini İndirme](../deployment/walkthrough-downloading-satellite-assemblies-on-demand-with-the-clickonce-deployment-api.md)
- [ClickOnce Uygulamalarını Yerelleştirme](../deployment/localizing-clickonce-applications.md)
