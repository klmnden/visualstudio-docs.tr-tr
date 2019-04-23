---
title: XSD görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
f1_keywords:
- vc.task.xsd
- VC.Project.VCXMLDataGeneratorTool.Namespace
- VC.Project.VCXMLDataGeneratorTool.GenerateFromSchema
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- XSD task (MSBuild (Visual C++))
- MSBuild (Visual C++), XSD task
ms.assetid: 15c99f5c-7124-4bbc-bc03-70c7bcce8893
caps.latest.revision: 16
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 44f25085edcc8b492946d54c7853f8ec32deb0c2
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60114970"
---
# <a name="xsd-task"></a>XSD Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir kaynaktan şema ya da sınıf dosyaları oluşturur XML şema tanımı Aracı (XSD.exe'nin) sarmalar.  
  
## <a name="parameters"></a>Parametreler  
 Parametreleri aşağıdaki tabloda açıklanmıştır **XSD** görev.  
  
- **AdditionalOptions**  
  
     İsteğe bağlı **dize** parametresi.  
  
     Komut satırında belirtilen seçeneklerin bir listesi. Örneğin, "*/option1 /option2 /option#*". Diğer tarafından temsil edilmez seçeneklerini belirtmek için bu parametreyi kullanın **XSD** görev parametresi.  
  
- **GenerateFromSchema**  
  
     İsteğe bağlı **dize** parametresi.  
  
     Belirtilen şemadan oluşturulan türler belirtir.  
  
     Her biri bir XSD seçeneğine karşılık gelir aşağıdaki değerlerden birini belirtin.  
  
    - **sınıflar** -   **/sınıfları**  
  
    - **veri kümesi** -   **/DataSet**  
  
- **Dil**  
  
     İsteğe bağlı **dize** parametresi.  
  
     Oluşturulan kod için kullanılacak programlama dilini belirtir.  
  
     Aralarından seçim **CS** (C#, varsayılan değerdir), **VB** (Visual Basic) veya **JS** (JScript). Ayrıca uygulayan bir sınıf için tam bir ad belirtin `System.CodeDom.Compiler.CodeDomProvider Class`.  
  
- **Namespace**  
  
     İsteğe bağlı **dize** parametresi.  
  
     Oluşturulan türleri için çalışma zamanı ad alanını belirtir.  
  
- **Kaynakları**  
  
     Gerekli `ITaskItem[]` parametresi.  
  
     Tüketilen ve görevler tarafından yayılan MSBuild kaynak dosya öğeleri bir dizisi tanımlanmaktadır.  
  
- **SuppressStartupBanner**  
  
     İsteğe bağlı **Boole** parametresi.  
  
     Varsa `true`, görev başladığında telif hakkı ve sürüm numarası iletisinin görüntülenmesini engeller.  
  
- **TrackerLogDirectory**  
  
     İsteğe bağlı **dize** parametresi.  
  
     İzleyici günlüğü dizini belirtir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görev Başvurusu](../msbuild/msbuild-task-reference.md)
