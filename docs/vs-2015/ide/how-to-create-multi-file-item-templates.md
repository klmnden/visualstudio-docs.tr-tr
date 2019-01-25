---
title: 'Nasıl yapılır: Çok dosyalı şablonlar oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- Visual Studio templates, creating multi-file item templates
- multi-file item templates
- item templates, creating multi-file item templates
ms.assetid: fe3c4257-e383-4c80-b8af-c5c521959c33
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 4616cb2f0e908b3228061288da05ce01543afdc4
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54785906"
---
# <a name="how-to-create-multi-file-item-templates"></a>Nasıl yapılır: Çok dosyalı öğe şablonları oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Öğe şablonları, yalnızca bir öğe belirtebilirsiniz, ancak öğe birden çok dosya bazen oluşur. Örneğin, bir Windows Forms öğe şablonu Visual Basic için aşağıdaki üç dosyayı gerektirir:  
  
- Form için kod içeren bir .vb dosyası.  
  
- Bir. form tasarımcısı bilgilerini içeren dosya Designer.vb olarak adlandırılır.  
  
- Form için gömülü kaynaklar içeren bir .resx dosyası.  
  
  Çok dosyalı öğe şablonları gerekli parametreleri doğru dosya adı uzantılarını öğesi oluşturulduğunda kullanılan emin olmak için [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Kullanarak bir öğe şablonu oluşturursanız **şablonu dışarı aktar** sihirbazında bu parametreleri otomatik olarak oluşturulur ve başka düzenleme gereklidir. Aşağıdaki adımlarda parametreleri doğru dosya adı uzantılarını oluşturulmasını sağlamak için nasıl kullanılacağını açıklanmaktadır.  
  
### <a name="to-manually-create-a-multi-file-item-template"></a>Çok dosyalı öğe şablonu el ile oluşturmak için  
  
1.  Öğe şablonu, tek dosyalı öğe şablonu oluşturacak şekilde oluşturun. Daha fazla bilgi için [nasıl yapılır: Öğe şablonları oluşturma](../ide/how-to-create-item-templates.md).  
  
2.  Ekleme `TargetFileName` her öznitelikleri `ProjectItem` öğesi. Değerlerini ayarlayın `TargetFileName` öznitelikleri için $fileinputname$. *FileExtension*burada *FileExtension* şablonuna dahil dosyasının dosya adı uzantısıdır. Örneğin:  
  
    ```  
    <ProjectItem TargetFileName="$fileinputname$.vb">  
        Form1.vb  
    </ProjectItem>  
    <ProjectItem TargetFileName="$fileinputname$.Designer.vb">  
        Form1.Designer.vb  
    </ProjectItem>  
    <ProjectItem TargetFileName="$fileinputname$.resx">  
        Form1.resx  
    </ProjectItem>  
    ```  
  
     Bu şablondan türetilmiş bir öğe için bir proje eklendiğinde, dosya adları, kullanıcı yazdığınız ad hesaplanır **Yeni Öğe Ekle** iletişim kutusu.  
  
3.  Şablonunuzda eklenmesi, seçime sağ tıklayın, dosyaları seçin **göndermek için**ve ardından **sıkıştırılmış (daraltılmış) klasör**. Seçtiğiniz dosyaların bir .zip dosyasına sıkıştırılır.  
  
4.  .Zip dosyasını kullanıcı öğe şablonu konuma yerleştirin. Varsayılan olarak, \My Documents\Visual Studio dizindir *sürüm*\Templates\ItemTemplates\\. Daha fazla bilgi için [nasıl yapılır: Şablonları bulma ve düzenleme](../ide/how-to-locate-and-organize-project-and-item-templates.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte gösterildiği bir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Windows Forms şablonu. Bu şablona dayalı bir öğe oluşturulduğunda oluşturulan üç dosyalarının adlarını girdiğiniz ad eşleşecektir **Yeni Öğe Ekle** iletişim kutusu.  
  
```  
<VSTemplate Version="2.0.0" Type="Item"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>Multi-file Item Template</Name>  
        <Icon>Icon.ico</Icon>  
        <Description>An example of a multi-file item template</Description>  
        <ProjectType>VisualBasic</ProjectType>  
    </TemplateData>  
    <TemplateContent>  
        <ProjectItem TargetFileName="$fileinputname$.vb" SubType="Form">  
            Form1.vb  
        </ProjectItem>  
        <ProjectItem TargetFileName="$fileinputname$.Designer.vb">  
            Form1.Designer.vb  
        </ProjectItem>  
        <ProjectItem TargetFileName="$fileinputname$.resx">  
            Form1.resx  
        </ProjectItem>  
    </TemplateContent>  
</VSTemplate>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)   
 [Nasıl yapılır: Öğe şablonları oluşturma](../ide/how-to-create-item-templates.md)   
 [Şablon parametreleri](../ide/template-parameters.md)   
 [Nasıl yapılır: Bir şablonda parametreleri ikame](../ide/how-to-substitute-parameters-in-a-template.md)
