---
title: Derleme bilgileri iletişim kutusu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- vb.ProjectPropertiesAssemblyInfo
helpviewer_keywords:
- Assembly Information dialog box
ms.assetid: 8f1f6449-e03d-4a5b-9076-d3b1f84ada48
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: dbcc8f31d00c270cf0eb9af8d3283a8674a639e3
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65703705"
---
# <a name="assembly-information-dialog-box"></a>Derleme Bilgileri İletişim Kutusu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

**Derleme bilgileri** iletişim kutusu değerlerini belirtmek için kullanılır [!INCLUDE[dnprdnshort](../../includes/dnprdnshort-md.md)] genel bütünleştirilmiş kod öznitelikleri, projenize otomatik olarak oluşturulan AssemblyInfo dosyasında depolanır. İçinde **Çözüm Gezgini**, dosya bulunan **Projem** düğümünde [!INCLUDE[vbprvb](../../includes/vbprvb-md.md)] (tıklayın **tüm dosyaları göster** görüntülemek için); altında bulunan  **Özellikleri** içinde [!INCLUDE[csprcs](../../includes/csprcs-md.md)]. Derleme öznitelikleri hakkında daha fazla bilgi için bkz: [öznitelikleri](https://msdn.microsoft.com/library/ae334cee-d96c-4243-a5e3-06dd7fcaf205).  
  
 Bu iletişim kutusuna erişmek için bir proje düğümü seçin **Çözüm Gezgini**ve ardından **proje** menüsünde tıklatın **özellikleri**. Zaman **Proje Tasarımcısı** görünen tıklayın **uygulama** sekmesi. Üzerinde **uygulama** sayfasında **derleme bilgilerini** düğmesi.  
  
## <a name="uielement-list"></a>UIElement Listesi  
 **Başlık**  
 Bütünleştirilmiş kod bildirimi için bir başlık belirtir. Karşılık gelen <xref:System.Reflection.AssemblyTitleAttribute>.  
  
 **Açıklama**  
 Bütünleştirilmiş kod bildirimi için isteğe bağlı bir açıklama belirtir. Karşılık gelen <xref:System.Reflection.AssemblyDescriptionAttribute>.  
  
 **Şirket**  
 Bütünleştirilmiş kod bildirimi için bir şirket adı belirtir. Karşılık gelen <xref:System.Reflection.AssemblyCompanyAttribute>.  
  
 **Ürün**  
 Bütünleştirilmiş kod bildirimi için ürün adını belirtir. Karşılık gelen <xref:System.Reflection.AssemblyProductAttribute>.  
  
 **Telif Hakkı**  
 Telif hakkı bildirimi bütünleştirilmiş kod bildirimi belirtir. Karşılık gelen <xref:System.Reflection.AssemblyCopyrightAttribute>.  
  
 **Ticari marka**  
 Bütünleştirilmiş kod bildirimi bir ticari marka belirtir. Karşılık gelen <xref:System.Reflection.AssemblyTrademarkAttribute>.  
  
 **Derleme sürümü**  
 Derlemenin sürümünü belirtir. Karşılık gelen <xref:System.Reflection.AssemblyVersionAttribute>.  
  
 **Dosya sürümü**  
 Belirli bir sürümü için Win32 dosya sürümü kaynak kullanılacağını derleyiciye bir sürüm numarasını belirtir. Karşılık gelen <xref:System.Reflection.AssemblyFileVersionAttribute>.  
  
 **GUID**  
 Derleme tanımlayan benzersiz bir GUID. Bir proje oluşturduğunuzda, Visual Studio derleme için bir GUID oluşturur. Karşılık gelen <xref:System.Guid>.  
  
 **Nötr dil**  
 Bu derlemenin desteklediği kültür belirtir. Karşılık gelen <xref:System.Resources.NeutralResourcesLanguageAttribute>. Varsayılan değer **(hiçbiri)**.  
  
 **Derlemeyi COM görünür yap**  
 Bütünleştirilmiş kodundaki türler COM'a olup olmadığını belirtir Karşılık gelen <xref:System.Runtime.InteropServices.ComVisibleAttribute>.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uygulama sayfası, Proje Tasarımcısı (Visual Basic)](../../ide/reference/application-page-project-designer-visual-basic.md)   
 [Öznitelikler](https://msdn.microsoft.com/library/ae334cee-d96c-4243-a5e3-06dd7fcaf205)
