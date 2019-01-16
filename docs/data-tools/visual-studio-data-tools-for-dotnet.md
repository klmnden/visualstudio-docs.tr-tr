---
title: .NET için veri araçları
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: c3175080-1dfb-4ab8-a460-92dadbb844b4
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
- dotnet
ms.openlocfilehash: 24da256ac835e477465845714cc844ac5bb305d7
ms.sourcegitcommit: 5a65ca6688a2ebb36564657d2d73c4b4f2d15c34
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "53872758"
---
# <a name="visual-studio-data-tools-for-net"></a>.NET için Visual Studio veri araçları

Visual Studio ve .NET Framework birlikte kapsamlı API ve araç veritabanlarına bağlanma, bellekte veri modelleme ve veri kullanıcı arabiriminde görüntülemek için desteği sağlar. Veri erişimi işlevleri sağlayan .NET Framework sınıfları olarak bilinen [ADO.NET](/dotnet/framework/data/adonet/index). Visual Studio'da araçları verileriyle birlikte bir ADO.NET, öncelikli olarak ilişkisel veritabanı ve XML desteklemek için tasarlanmıştır. Bugünlerde çoğu NoSQL veritabanı satıcıların veya üçüncü taraflar, ADO.NET sağlayıcılar sunar.

[.NET core](/dotnet/core/) ADO.NET veri kümeleri ve ilgili türler hariç destekler. .NET Core'u hedefleyen ve bir nesne ilişkisel eşleme (ORM) katmanı gerektirir, kullanmanız [Entity Framework Core](/ef/core/).

Aşağıdaki diyagram, temel mimarisinin basitleştirilmiş bir görünümünü gösterir:

![ADO.NET mimarisi](../data-tools/media/raddata-ado-net-architecture-diagram.png)

## <a name="typical-workflow"></a>Tipik iş akışı

Tipik iş akışı şudur:

1. Geliştirme veya test veritabanı yerel makinenize yükleyin. Bkz: [veritabanı sistemleri, araçları ve örnek yükleme](../data-tools/installing-database-systems-tools-and-samples.md). Bir Azure veri hizmeti kullanıyorsanız, bu adım gerekli değildir.

2. Veritabanı (veya hizmet veya yerel dosya) bağlantı, Visual Studio'da test edin. Bkz: [yeni bağlantı ekleme](../data-tools/add-new-connections.md).

3. (İsteğe bağlı) Oluştur ve yeni bir modeli yapılandırmak için araçları kullanın. Entity Framework tabanlı yeni uygulamalar için varsayılan öneriyi modelleridir. Modelin hangi birini kullanın, uygulama ile etkileşime giren veri kaynağıdır. Modeli, veritabanı veya hizmet ve uygulama arasında mantıksal olarak bulunur. Bkz: [yeni veri kaynağı ekleme](../data-tools/add-new-data-sources.md).

4. Veri kaynağından sürükleyin **veri kaynakları** verilerin belirttiğiniz şekilde kullanıcıya görüntülenecek veri bağlama kodunu oluşturmak için bir Windows Forms, ASP.NET veya Windows Presentation Foundation tasarım yüzeyine penceresi. Bkz: [Visual Studio'da verilere denetimler bağlama](../data-tools/bind-controls-to-data-in-visual-studio.md).

5. Temel alınan veritabanına gösteren özel işlevsellikten yararlanmak için veya iş kuralları, arama ve veri doğrulama gibi şeyler için özel kod ekleyin.

3. adımına geçin ve sorunu komutları doğrudan bir model kullanmak yerine bir veritabanı için bir .NET uygulaması programı. Bu durumda, ilgili belgeleri burada bulabilirsiniz: [ADO.NET](/dotnet/framework/data/adonet/index). Kullanmaya devam edebilirsiniz Not **veri kaynağı Yapılandırma Sihirbazı** ve tasarımcılar, bellek ve bu nesnelere veri bağlama UI denetimleri kendi nesnelerinizi doldururken veri bağlama kodunu oluşturmak için.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da verilere erişime](../data-tools/accessing-data-in-visual-studio.md)