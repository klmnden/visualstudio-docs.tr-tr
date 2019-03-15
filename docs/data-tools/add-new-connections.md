---
title: Yeni bağlantı ekleme
ms.date: 11/04/2016
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: b01af2aa269cbaddbd84d24827b1a77e97d52d8a
ms.sourcegitcommit: 4ffb7be5384ad566ce46538032bf8561754c61a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2019
ms.locfileid: "57982811"
---
# <a name="add-new-connections"></a>Yeni bağlantı ekleme

Bir veritabanı veya hizmet bağlantınızı test etmek ve veritabanı içeriklerini ve şemaları kullanarak keşfetme **Sunucu Gezgini**, **Cloud Explorer**, veya **SQL Server Nesne Gezgini**. Bu windows işlevlerini, bir aşamaya çakışıyor. Temel farklılıklar şunlardır:

- Server Explorer

   Visual Studio'da varsayılan olarak yüklüdür. Bağlantılarını test et ve SQL Server veritabanları, bir ADO.NET sağlayıcısı yüklü olan herhangi bir veritabanına ve bazı Azure hizmetleri görüntülemek için kullanılabilir. Ayrıca Sistem performans sayaçları, olay günlükleri ve ileti kuyrukları gibi alt düzey nesneleri gösterir. Bir veri kaynağına ADO.NET sağlayıcısı yok varsa, burada gösterilmez, ancak bunu Visual Studio'dan programlı bir şekilde bağlanarak kullanmaya devam edebilirsiniz.

- Cloud Explorer

   Bu pencere, bir Visual Studio uzantı olarak el ile yükleme [Visual Studio Market](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.CloudExplorerForVS). İçin keşfetmek ve Azure hizmetlerine bağlanan özel işlevler sağlar.

- SQL Server Object Explorer

   SQL Server veri araçları ile birlikte yüklenir ve altında görünür **görünümü** menüsü. Burada görmüyorsanız, Git **programlar ve Özellikler** Denetim Masası ' nda Visual Studio'yu bulun ve ardından **değişiklik** SQL Server veri araçları için onay kutusunu işaretledikten sonra yükleyiciyi yeniden çalıştırın. Kullanım **SQL Server Nesne Gezgini** görünümü SQL veritabanlarına (bir ADO.NET sağlayıcısı yüklü değilse), yeni veritabanları oluşturmak, şemalar değiştirmek, saklı yordamlar oluşturma, bağlantı dizelerini almak, veri ve daha fazlasını görüntüleyin. Hiçbir ADO.NET sağlayıcısı yüklü olan SQL veritabanları burada gösterilmez, ancak yine de bunları programlı bir şekilde bağlanabilirsiniz.

## <a name="add-a-connection-in-server-explorer"></a>Sunucu Gezgini'nde bir bağlantı Ekle

Veritabanına bir bağlantı oluşturmak için tıklayın **Bağlantı Ekle** simgesini **Sunucu Gezgini**, ya da sağ **Sunucu Gezgini** üzerinde **veri Bağlantıları** düğümünü seçip alt **Bağlantı Ekle**. Buradan, başka bir sunucu, bir SharePoint hizmet veya bir Azure hizmeti bir veritabanına bağlanabilirsiniz.

![Sunucu Gezgini yeni bağlantı simgesi](../data-tools/media/raddata-server-explorer-new-connection-icon.png)

Bu işlem sonrasında **Bağlantı Ekle** iletişim kutusu. Burada, biz SQL Server LocalDB örneğinin adı girdiniz.

![Yeni Bağlantı Ekle](../data-tools/media/raddata-add-new-connection-dialog.png)

## <a name="change-the-provider"></a>Sağlayıcısını değiştirme

Veri kaynağı istemezsiniz tıklayarak **değişiklik** düğmesi, yeni bir veri kaynağı ve/veya yeni bir ADO.NET veri sağlayıcı seçin. Yeni sağlayıcıyı nasıl yapılandırdığınıza bağlı olarak, kimlik bilgilerini isteyebilir.

![Değişiklik AD0.NET veri sağlayıcısı](../data-tools/media/raddata-change-ad0.net-data-provider.png)

## <a name="test-the-connection"></a>Bağlantıyı test edin

Veri kaynağını seçtikten sonra tıklayın **Bağlantıyı Sına**. Başarısız olursa sorun gidermek satıcı belgelerine göre ihtiyacınız olacak.

![Bağlantıyı test et](../data-tools/media/raddata-test-connection.png)

Test başarılı olursa oluşturmaya hazır olduğunuz bir *veri kaynağı*, gerçekten anlamına gelen bir Visual Studio terimi olduğu bir *veri modeli* temel alınan veritabanı veya hizmet tabanlı.

## <a name="see-also"></a>Ayrıca bkz.

- [.NET için Visual Studio veri araçları](../data-tools/visual-studio-data-tools-for-dotnet.md)
