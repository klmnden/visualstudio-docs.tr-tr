---
title: 'Nasıl yapılır: Çoğullaştırmayı açıp (O R Designer) kapatma'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 9b693bc3-303a-40a9-97ee-9cef5ca3ae81
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 769d1760692cad6a6b813ece16d69f4abd3d26b1
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63402775"
---
# <a name="how-to-turn-pluralization-on-and-off-or-designer"></a>Nasıl yapılır: Çoğullaştırmayı açıp (O/R Tasarımcısı) kapatma
Varsayılan olarak, s ya da gelen zellikleri sonlanan adlara sahip veritabanı nesneleri sürüklediğinizde **Sunucu Gezgini** veya **veritabanı Gezgini** üzerine [LINQ to SQL araçları Visual Studio'da](../data-tools/linq-to-sql-tools-in-visual-studio2.md), üretilen varlık sınıflarının adları çoğul için tekil değiştirilir. Bu, daha doğru bir şekilde oluşturulan varlık sınıfı verilerin tek bir kaydına eşler olgu temsil etmek için gerçekleştirilir. Örneğin, bir `Customers` tablo **O/R Tasarımcısı** sonuçları adlı bir varlık sınıfında `Customer` sınıfın yalnızca tek bir müşterinin verilerini tutacak çünkü.

> [!NOTE]
> Çoğullaştırma yalnızca İngilizce sürümü Visual Studio'nun içinde varsayılan olarak açıktır.

[!INCLUDE[note_settings_general](../data-tools/includes/note_settings_general_md.md)]

### <a name="to-turn-pluralization-on-and-off"></a>Çoğullaştırmayı açıp kapatmak için

1. Üzerinde **Araçları** menüsünü tıklatın **seçenekleri**.

2. İçinde **seçenekleri** iletişim kutusunda **veritabanı araçları**.

    > [!NOTE]
    > Seçin **tüm ayarları göster** varsa **veritabanı araçları** düğümü görünür değil.

3. Tıklayın **O/R Tasarımcısı**.

4. Ayarlama **adların Çoğullaştırılmasını** için **etkin** = **False** ayarlanacak **O/R Tasarımcısı** böylece sınıf adları değiştirmez .

5. Ayarlama **adların Çoğullaştırılmasını** için **etkin** = **True** eklenen nesneleri sınıf adlarını çoğullaştırma kuralları uygulamak için **O/R Tasarımcı**.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
- [LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/index)
- [Visual Studio'da verilere erişime](../data-tools/accessing-data-in-visual-studio.md)