---
title: FileClassifier görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- classifying a resource set to embed in an assembly [WPF MSBuild]
- non-localizable resources [WPF MSBuild], classifying to embed in an assembly
- FileClassifier task [WPF MSBuild]
ms.assetid: 14e03310-fcc0-4bb2-a84d-cda12be66367
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e14ff5857676746c630bc8a7187571d3adb8f4e8
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53820767"
---
# <a name="fileclassifier-task"></a>FileClassifier görevi
<xref:Microsoft.Build.Tasks.Windows.FileClassifier> Görev bir bütünleştirilmiş kod içine katıştırılmış olarak kaynak kaynak kümesini sınıflandırır. Bir kaynak yerelleştirilebilir değil ise, ana uygulama derlemesine eklenir; Aksi takdirde, bir uydu derlemeye eklenir.  
  
## <a name="task-parameters"></a>Görev parametreleri  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`CLREmbeddedResource`|Kullanılmayan.|  
|`CLRResourceFiles`|Kullanılmayan.|  
|`CLRSatelliteEmbeddedResource`|Kullanılmayan.|  
|`Culture`|İsteğe bağlı **dize** parametresi.<br /><br /> Derleme için kullanılacak kültürü belirtir. Bu değer **null** derleme yerelleştirilemeyen ise. Varsa **null**, küçük değer varsayılan değerdir **CultureInfo.InvariantCulture** döndürür.|  
|`MainEmbeddedFiles`|İsteğe bağlı **Itaskıtem []** çıkış parametresi.<br /><br /> Ana derleme gömülü yerelleştirilemeyen kaynaklar belirtir.|  
|`OutputType`|Gerekli **dize** parametresi.<br /><br /> Belirtilen kaynak dosyalarıyla katıştırmak için dosya türünü belirtir. Geçerli değerler **exe**, **winexe**, veya **Kitaplığı**.|  
|`SatelliteEmbeddedFiles`|İsteğe bağlı **Itaskıtem []** çıkış parametresi.<br /><br /> Belirtilen kültür için uydu derlemesine gömülür yerelleştirilebilir dosyaları belirtir **kültür** parametresi.|  
|`SourceFiles`|Gerekli **Itaskıtem []** parametresi.<br /><br /> Dosyaları sınıflandırmak için listesini belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Varsa **kültür** parametresi ayarlanmadı, kullanılarak belirtilen tüm kaynakların **Kaynakdosyalar** parametresi yerelleştirilemeyen; bir ileilişkiliolduklarısüreceAksitakdirde,bunlaryerelleştirilebilir **Yerelleştirilebilir** ayarlanan öznitelik **false**.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, tek bir kaynak dosyasını kaynak olarak sınıflandırır ve French-Canadian (fr-CA) kültür için bir uydu derlemeye katıştırır.  
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  <UsingTask  
    TaskName="Microsoft.Build.Tasks.Windows.FileClassifier"   
    AssemblyFile="C:\Program Files\Reference Assemblies\Microsoft\Framework\v3.0\PresentationBuildTasks.dll" />  
  <ItemGroup>  
    <Resource Include="Resource1.bmp" />  
  </ItemGroup>  
  <Target Name="FileClassifierTask">  
    <FileClassifier  
      SourceFiles="Resource1.bmp"  
      Culture="fr-CA"  
      OutputType="exe" />  
  </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [WPF MSBuild başvurusu](../msbuild/wpf-msbuild-reference.md)   
 [Görev başvurusu](../msbuild/wpf-msbuild-task-reference.md)   
 [MSBuild başvurusu](../msbuild/msbuild-reference.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)   
 [Bir WPF uygulaması (WPF) oluşturma](/dotnet/framework/wpf/app-development/building-a-wpf-application-wpf)