---
title: MSBuild hedeflerini kullanarak SharePoint çözüm paketini özelleştirme
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, packages
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 71665f6ccf22ace264ff39831521538a335aed93
ms.sourcegitcommit: 25570fb5fb197318a96d45160eaf7def60d49b2b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/30/2019
ms.locfileid: "66401505"
---
# <a name="how-to-customize-a-sharepoint-solution-package-by-using-msbuild-targets"></a>Nasıl yapılır: MSBuild hedeflerini kullanarak SharePoint çözüm paketini özelleştirme
  Bir komut isteminde MSBuild hedeflerini kullanarak Visual Studio SharePoint paket dosyaları nasıl oluşturduğunu özelleştirebilirsiniz ( *.wsp*). Örneğin, paketleme Ara dizin ve numaralandırılmış dosyaları belirttiğiniz MSBuild öğesi gruplarını değiştirmek için MSBuild özelliklerini de özelleştirebilirsiniz.

## <a name="customize-and-run-msbuild-targets"></a>Özelleştirme ve MSBuild hedefleri çalıştırın
 BeforeLayout ve AfterLayout hedefleri özelleştirirseniz, önce paket düzeni, ekleme, kaldırma veya paketlenmiş dosyalarını değiştirme gibi görevler gerçekleştirebilirsiniz.

#### <a name="to-customize-the-beforelayout-target"></a>BeforeLayout hedef özelleştirmek için

1. Not Defteri gibi bir düzenleyici açın ve ardından aşağıdaki kodu ekleyin.

   ```xml
   <Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
     <Target Name="BeforeLayout">
       <Message Importance="high" Text="In the BeforeLayout Target"></Message>
     </Target>
   </Project>
   ```

    Bu örnekte, önce bu hedef paketleme bir ileti görüntüler.

2. Dosya adı **CustomLayout.SharePoint.targets**ve SharePoint proje klasörüne kaydedin.

3. Projeyi açmak için kısayol menüsünü açın ve ardından **projeyi**.

4. İçinde **Çözüm Gezgini**, proje için kısayol menüsünü açın ve ardından **Düzenle**  *\<ProjectName > .vbproj* veya **Düzenle**  *\<ProjectName > .csproj*.

5. Sonra `Import` proje dosyasının sonuna satır, aşağıdaki satırı ekleyin.

   ```xml
   <Import Project="CustomLayout.SharePoint.targets" />
   ```

6. Proje dosyasını kaydedip kapatın.

7. İçinde **Çözüm Gezgini**, proje için kısayol menüsünü açın ve ardından **projeyi**.

   Proje yayımladığınızda, paketleme başlamadan önce ileti çıktıda görünür.

#### <a name="to-customize-the-afterlayout-target"></a>AfterLayout hedef özelleştirmek için

1. Menü çubuğunda, **dosya** > **açık** > **dosya**.

2. İçinde **açık dosya** iletişim kutusunda proje klasörüne gidin, CustomLayout.target dosyayı seçin ve ardından **açık** düğmesi.

3. Hemen önce `</Project>` etiketi, aşağıdaki kodu ekleyin:

   ```xml
   <Target Name="AfterLayout">
     <Message Importance="high" Text="In the AfterLayout Target"></Message>
   </Target>
   ```

    Bu örnekte, bu hedef paketlenmiştir sonra bir ileti görüntüler.

4. Hedefleri dosyasını kaydedip kapatın.

5. Visual Studio'yu yeniden başlatın ve sonra projeyi açabilirsiniz.

   Proje yayımladığınızda, başlatılmadan önce paketleme BeforeLayout iletisi görüntülenir ve paketleme bittikten sonra AfterLayout iletisi görüntülenir.

## <a name="see-also"></a>Ayrıca bkz.
- [Paketleme ve SharePoint çözümlerini dağıtma](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)
