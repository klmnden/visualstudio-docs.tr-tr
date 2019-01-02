---
title: 'Nasıl Yapılır: MSBuild görevleri kullanarak SharePoint çözüm paketini oluşturun | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, packages
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: a9a954c00c616ff156d786386c92d41dcbe85c13
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53818332"
---
# <a name="how-to-create-a-sharepoint-solution-package-by-using-msbuild-tasks"></a>Nasıl Yapılır: MSBuild görevleri kullanarak bir SharePoint çözüm paketini oluşturma
  Derleme, temizleme ve bir SharePoint paketi doğrulama (*.wsp*) geliştirme bilgisayarında komut satırı MSBuild görevleri kullanarak. Bu komutları, yapı bilgisayarında Team Foundation Server'ı kullanarak yapı sürecinin otomatik hale getirmek için de kullanabilirsiniz.  
  
## <a name="build-a-sharepoint-package"></a>Bir SharePoint paketi oluşturun  
  
#### <a name="to-build-a-sharepoint-package"></a>Bir SharePoint paketi oluşturmak için  
  
1.  Windows üzerinde **Başlat** menüsünde seçin **tüm programlar** > **Donatılar** > **komut istemi**.  
  
2.  SharePoint projenizi bulunduğu dizine geçin.  
  
3.  Proje için bir paket oluşturmak için aşağıdaki komutu girin. Değiştirin *ProjectFileName* ile projenin adı.  
  
    ```cmd  
    msbuild /t:Package ProjectFileName  
    ```  
  
     Örneğin, ListDefinition1 adlı bir SharePoint projesi paketlemek için aşağıdaki komutlardan birini çalıştırabilirsiniz.  
  
    ```cmd  
    msbuild /t:Package ListDefinition1.vbproj  
    msbuild /t:Package ListDefinition1.csproj  
    ```  
  
## <a name="clean-a-sharepoint-package"></a>SharePoint paketinin Temizle  
  
#### <a name="to-clean-a-sharepoint-package"></a>SharePoint paketinin temizlemek için  
  
1.  Bir komut istemi penceresi açın.  
  
2.  SharePoint projenizi bulunduğu dizine geçin.  
  
3.  Proje için bir paket temizlemek için aşağıdaki komutu girin. Değiştirin *ProjectFileName* ile projenin adı.  
  
    ```cmd  
    msbuild /t:CleanPackage ProjectFileName  
    ```  
  
     Örneğin, ListDefinition1 adlı bir SharePoint projesi temizlemek için aşağıdaki komutlardan birini çalıştırabilirsiniz.  
  
    ```cmd  
    msbuild /t:CleanPackage ListDefinition1.vbproj  
    msbuild /t:CleanPackage ListDefinition1.csproj  
    ```  
  
## <a name="validate-a-sharepoint-package"></a>Bir SharePoint paketi doğrulama  
  
#### <a name="to-validate-a-sharepoint-package"></a>Bir SharePoint paketi doğrulamak için  
  
1.  Bir komut istemi penceresi açın.  
  
2.  SharePoint projenizi bulunduğu dizine geçin.  
  
3.  Proje için bir paket doğrulamak için aşağıdaki komutu girin. Değiştirin *ProjectFileName* ile projenin adı.  
  
    ```cmd  
    msbuild /t:ValidatePackage ProjectFileName  
    ```  
  
     Örneğin, ListDefinition1 adlı bir SharePoint projesi doğrulamak için aşağıdaki komutlardan birini çalıştırabilirsiniz.  
  
    ```cmd  
    msbuild /t:ValidatePackage ListDefinition1.vbproj  
    msbuild /t:ValidatePackage ListDefinition1.csproj  
    ```  
  
## <a name="set-properties-in-a-sharepoint-package"></a>Bir SharePoint paketi özelliklerini ayarlama  
  
#### <a name="to-set-a-property-in-a-sharepoint-package"></a>Bir SharePoint paketi özellik ayarlamak için  
  
1.  Bir komut istemi penceresi açın.  
  
2.  SharePoint projenizi bulunduğu dizine geçin.  
  
3.  Proje için bir paket içindeki bir özelliği ayarlamak için aşağıdaki komutu girin. Değiştirin *PropertyName* ayarlamak istediğiniz özelliği.  
  
    ```cmd  
    msbuild /property:PropertyName=Value  
    ```  
  
     Örneğin, uyarı düzeyini ayarlamak için aşağıdaki komutu çalıştırabilirsiniz.  
  
    ```cmd  
    msbuild /property:WarningLevel = 2  
    ```  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint özellikleri oluşturma](../sharepoint/creating-sharepoint-features.md)   
 [Nasıl yapılır: Bir SharePoint özelliğini özelleştirme](../sharepoint/how-to-customize-a-sharepoint-feature.md)   
 [Nasıl yapılır: SharePoint özelliklerine öğe ekleyip](../sharepoint/how-to-add-and-remove-items-to-sharepoint-features.md)  
