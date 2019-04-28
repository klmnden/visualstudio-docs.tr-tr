---
title: Başvurular sayfası, Proje Tasarımcısı (Visual Basic) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- vb.ProjectPropertiesReference
- vb.ProjectPropertiesUnusedReference
- vb.ProjectPropertiesReferencePaths
helpviewer_keywords:
- References page in Project Designer
- Project Designer, References page
- Unused References dialog box
ms.assetid: 5a47c595-e084-401c-86e1-74e0bf74fd86
caps.latest.revision: 40
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: a714c3b3b282d37e4f8c9e73a593c9a35298f151
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63443838"
---
# <a name="references-page-project-designer-visual-basic"></a>Başvurular Sayfası, Proje Tasarımcısı (Visual Basic)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Kullanım **başvuruları** sayfasının **Proje Tasarımcısı** başvuruları ve Web başvuruları projenize içeri aktarılan ad alanlarını yönetmek için. Proje başvuruları COM bileşenlerini, XML Web Hizmetleri, .NET Framework sınıf kitaplıkları veya derlemeleri ve diğer sınıf kitaplıkları için içerebilir. Başvuruları kullanma hakkında daha fazla bilgi için bkz. [bir projedeki başvuruları yönetme](../../ide/managing-references-in-a-project.md).  
  
 Erişim için **başvuruları** sayfasında, bir proje düğümü seçin (değil **çözüm** düğümü) içinde **Çözüm Gezgini**. Ardından **proje**, **özellikleri** menü çubuğundaki. Proje Tasarımcısı göründüğünde tıklayın **başvuruları** sekmesi.  
  
## <a name="uielement-list"></a>UIElement Listesi  
 Aşağıdaki seçenekler seçin veya projenize başvurular ve içeri aktarılan ad alanlarını kaldırma olanak sağlar.  
  
 **Kullanılmayan başvurular**  
 Erişim için bu düğmeye tıklayın **kullanılmayan başvurular** iletişim kutusu.  
  
 **Kullanılmayan başvurular** iletişim kutusu, projenize dahil olan, ancak aslında kod tarafından kullanılan başvuruları kaldırın olanak tanır. Listeleyen bir kılavuz içerdiği **başvuru adı**, **yolu**, ilgili, projedeki kullanılmayan ad alanı başvuruları ve diğer bilgileri. Kılavuzda tıklatıp projenizden kaldırmak istediğiniz ad alanı başvurularını seçin **Kaldır**.  
  
 **Başvuru yolları**  
 Erişim için bu düğmeye tıklayın **başvuru yolları** iletişim kutusu.  
  
> [!NOTE]
> Proje sistemi bir bütünleştirilmiş kod başvurusu bulduğunda, sistem aşağıdaki sırayla şu konumlarda bakarak başvuru çözer:  
> 
> 1. Proje klasörü. Proje klasörü dosyaları görünür **Çözüm Gezgini** olduğunda **tüm dosyaları göster** geçerli değildir.  
>    2. İçinde belirtilen klasörler **başvuru yolları** iletişim kutusu.  
>    3. Dosyaları görüntüleme klasörleri **Başvuru Ekle** iletişim kutusu.  
>    4. Projenin obj klasörü. (Bir veya daha fazla derlemeleri projenize bir COM başvurusu eklediğinizde, projenin obj klasöre eklenebilir.)  
  
 **Başvurular**  
 Bu liste, projede kullanılan tüm başvuruları gösterir veya kullanılmayan.  
  
 **Add**  
 Bir başvuru veya Web başvurusu eklemek için bu düğmeye tıklayın **başvuruları** listesi.  
  
 Seçin **başvuru** Başvuru Ekle iletişim kutusunu kullanarak projenize bir başvuru eklemek için.  
  
 Seçin **Web başvurusu** projenize Web Başvurusu Ekle iletişim kutusunu kullanarak bir Web başvurusu eklemek için.  
  
 **Kaldır**  
 Bir veya daha fazla başvurularını seçin **başvuruları** listelemek ve silmek için bu düğmeye tıklayın.  
  
 **Web başvurusunu güncelleştir**  
 Bir Web başvurusu seçin **başvuruları** listelemek ve güncelleştirmek için bu düğmeye tıklayın.  
  
 **İçeri aktarılan ad alanları**  
 Bu kutusuna kendi ad alanı ve tıklayın **kullanıcı içeri aktarma ekleyin** ad alanları listesine eklenecek.  
  
 Kullanıcı içeri aktarılan ad alanları için diğer adlar oluşturabilirsiniz. Bunu yapmak için diğer ad ve ad alanı biçiminde girin *diğer*=*ad alanı*. Örneğin uzun ad kullanıyorsanız kullanışlıdır: `Http= MyOrg.ObjectLib.Internet.WebRequestMethods.Http`.  
  
 **Kullanıcı içeri aktarma ekleyin**  
 Belirtilen ad alanı eklemek için bu düğmeye tıklayın **içeri aktarılan ad alanlarını** liste kutusuna içeri aktarılan ad alanları. Düğme, yalnızca belirtilen ad alanı zaten listede değilse etkindir.  
  
 **Ad alanları listesi**  
 Tüm kullanılabilir ad alanlarının bu listede gösterilir. Projenize dahil olan ad alanları için onay kutularını seçilir.  
  
 **Güncelleştirme kullanıcı içeri aktarma**  
 Ad alanları listesinde bir kullanıcı tarafından belirtilen ad alanı seçin, içinde değiştirmek istediğiniz adı yazın **içeri aktarılan ad alanlarını** kutusuna ve ardından yeni bir ad alanına değiştirmek için bu düğmeye tıklayın. Düğme seçili ad alanı kullanılarak listeye eklenen bir ise etkinleştirilmeden **kullanıcı içeri aktarma eklemek** düğmesi. Ekleyebilirsiniz:  
  
- Sınıf veya ad alanları gibi <xref:System.Math?displayProperty=fullName>.  
  
- Diğer adlı alır, gibi `VB=Microsoft.VisualBasic`.  
  
- XML ad alanları gibi `<xmlns:xsl="http://www.w3.org/1999/XSL/Transform">`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [NIB nasıl yapılır: Başvuru Ekle iletişim kutusunu kullanarak başvuruları kaldırın veya ekleyin](http://msdn.microsoft.com/3bd75d61-f00c-47c0-86a2-dd1f20e231c9)   
 [Nasıl yapılır: Ekleme veya kaldırma içeri aktarılan ad alanlarını (Visual Basic)](../../ide/how-to-add-or-remove-imported-namespaces-visual-basic.md)   
 [NIB: Web Başvurusu Ekle iletişim kutusu](http://msdn.microsoft.com/bdf05776-c591-40af-bfd7-e1e2aa1e87b5)   
 [Imports Deyimi (XML Ad Alanı)](http://msdn.microsoft.com/library/1f4d50a6-08c7-4c2e-8206-ccae35fcd1b4)
