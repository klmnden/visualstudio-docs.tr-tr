---
title: 'Nasıl yapılır: Çoğullaştırmayı açıp (O R Designer) kapatma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-data-tools
ms.topic: conceptual
ms.assetid: 9b693bc3-303a-40a9-97ee-9cef5ca3ae81
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: c8497f63e2b4dc51caa69b1babe0d707e8370aab
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65704949"
---
# <a name="how-to-turn-pluralization-on-and-off-or-designer"></a>Nasıl yapılır: Çoğullaştırmayı açıp (O/R Tasarımcısı) kapatma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Varsayılan olarak, s ya da gelen zellikleri sonlanan adlara sahip veritabanı nesneleri sürüklediğinizde **Sunucu Gezgini**/**veritabanı Gezgini** üzerine [LINQ to SQL araçlarını Visual Studio'da](../data-tools/linq-to-sql-tools-in-visual-studio2.md), tekil için üretilen varlık sınıflarının ad çoğul olarak değiştirilir. Bu, daha doğru bir şekilde oluşturulan varlık sınıfı verilerin tek bir kaydına eşler olgu temsil etmek için gerçekleştirilir. Örneğin, bir Müşteriler tablosunu ekleme [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)] sınıfın yalnızca tek bir müşterinin verilerini tutacak çünkü bir varlık sınıfı sonuçlarında adlı müşteri.  
  
> [!NOTE]
> Çoğullaştırma yalnızca İngilizce sürümü Visual Studio'nun içinde varsayılan olarak açıktır.  
  
 [!INCLUDE[note_settings_general](../includes/note-settings-general-md.md)]  
  
### <a name="to-turn-pluralization-on-and-off"></a>Çoğullaştırmayı açıp kapatmak için  
  
1. Üzerinde **Araçları** menüsünü tıklatın **seçenekleri**.  
  
2. İçinde **seçenekleri** iletişim kutusunda **veritabanı araçları**.  
  
> [!NOTE]
> Seçin **tüm ayarları göster** varsa **veritabanı araçları** düğümü görünür değil.  
  
1. Tıklayın **O/R Tasarımcısı**.  
  
2. Ayarlama **adların Çoğullaştırılmasını** için **etkin** = **False** ayarlanacak [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)] böylece sınıf adları değiştirmez.  
  
3. Ayarlama **adların Çoğullaştırılmasını** için **etkin** = **True** eklenen nesneleri sınıf adlarını çoğullaştırma kuralları uygulamak için [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)].  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [LINQ to SQL araçlarını Visual Studio'da](../data-tools/linq-to-sql-tools-in-visual-studio2.md)   
 [LINQ to SQL](https://msdn.microsoft.com/library/73d13345-eece-471a-af40-4cc7a2f11655)   
 [Visual Studio'da verilere erişime](../data-tools/accessing-data-in-visual-studio.md)
