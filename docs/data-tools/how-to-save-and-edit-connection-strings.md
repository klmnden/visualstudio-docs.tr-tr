---
title: 'Nasıl Yapılır: Kaydetme ve bağlantı dizeleri düzenleme'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: f8ef3a2c-029c-423b-9d9e-a4f1add4f640
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: 96c55b44e6e6ebbfba27c4daf10512cefe1fd393
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53961276"
---
# <a name="how-to-save-and-edit-connection-strings"></a>Nasıl Yapılır: Bağlantı dizelerini kaydetme ve düzenleme
Visual Studio uygulamalarında bağlantı dizeleri (uygulama ayarları da bilinir) uygulama yapılandırma dosyasında kaydedilen veya doğrudan uygulamanıza sabit kodlanmış. Uygulama yapılandırma dosyasında bağlantı dizelerini kaydetme, uygulamanızın sürdürme görevini basitleştirir. Bağlantı dizesi değiştirilmesi gerekiyorsa (aksine, kaynak kodunda değiştirin ve uygulamayı yeniden derlemenize gerek) uygulama ayarları dosyasında güncelleştirebilirsiniz.

(Parola gibi) hassas bilgiler bağlantı dizesi içinde depolamak, uygulamanızın güvenliğini etkileyebilir. Bağlantı dizeleri uygulama yapılandırma dosyasına kaydedildi şifrelenmez veya gizlenmiş birisi için dosyaya erişim ve içeriğini görüntülemek mümkün olabilir. Windows tümleşik güvenlik'i kullanarak bir veritabanına erişimi denetlemek için daha güvenli bir yoludur.

Kullanmayı seçmezseniz Windows tümleşik güvenliğini ve veritabanınızı bir kullanıcı adı ve parola gerektirir, bağlantı dizesinden atlayabilirsiniz, ancak uygulamanız başarıyla veritabanına bağlanmak için bu bilgileri sağlamanız gerekir. Örneğin, bağlantı dizesini çalışma zamanında dinamik olarak oluşturur ve bu bilgileri kullanıcıya sorar bir iletişim kutusu oluşturabilirsiniz. Veritabanı postası bilgileri yakalanırsa güvenlik sorunu olmaya devam edebilir.
Daha fazla bilgi için [bağlantı bilgilerini koruma](/dotnet/framework/data/adonet/protecting-connection-information).

## <a name="to-save-a-connection-string-from-within-the-data-source-configuration-wizard"></a>Veri Kaynağı Yapılandırma Sihirbazı içinde bir bağlantı dizesini kaydetmek için
İçinde **veri kaynağı Yapılandırma Sihirbazı**, bağlantıyı kaydetmek için seçeneğini **bağlantı dizesini uygulama yapılandırma dosyasına Kaydet** sayfası.

## <a name="to-save-a-connection-string-directly-into-application-settings"></a>Uygulama ayarlarına doğrudan bir bağlantı dizesini kaydetmek için
1. İçinde **Çözüm Gezgini**, çift **Projem** simgesi (Visual Basic) veya **özellikleri** simgesi (C#) açmak için **ProjeTasarımcısı**.
1. Seçin **ayarları** sekmesi.
1. Girin bir **adı** bağlantı dizesi. Bu ada kod bağlantı dizesinde erişirken bakın.
1. Ayarlama **türü** için (**bağlantı dizesi**).
1. Bırakın **kapsam** kümesine **uygulama**.
1. Bağlantı dizenizi girin **değer** tıklayın veya alanı **üç nokta** (...) düğmesini **değer** açmak için alan **bağlantıözellikleri** bağlantı dizenizi oluşturmak için iletişim kutusu.

## <a name="edit-connection-strings-stored-in-application-settings"></a>Uygulama ayarlarında depolanan bağlantı dizeleri düzenleme
Uygulama ayarlarını kullanarak kaydedilen bağlantı bilgilerini değiştirebileceğiniz **Proje Tasarımcısı**.

### <a name="to-edit-a-connection-string-stored-in-application-settings"></a>Bir bağlantı dizesi uygulama ayarlarında depolanan düzenlemek için
1. İçinde **Çözüm Gezgini**, çift **Projem** simgesi (Visual Basic) veya **özellikleri** simgesi (C#) açmak için **ProjeTasarımcısı**.
1. Seçin **ayarları** sekmesi.
1. Bulmak istediğiniz metni düzenleyin ve bağlantıyı **değer** alan.
1. Bağlantı dizesini Düzenle **değer** tıklayın veya alanı **üç nokta** (...) düğmesini **değer** bağlantınızla düzenlemek için alan **bağlantı Özellikleri** iletişim kutusu.

## <a name="edit-connection-strings-for-datasets"></a>Veri kümeleri için bağlantı dizelerini Düzenle
Bir veri kümesindeki her bir TableAdapter için bağlantı bilgilerini değiştirebilirsiniz.

### <a name="to-edit-a-connection-string-for-a-tableadapter-in-a-dataset"></a>Bir veri kümesinde bir TableAdapter için bir bağlantı dizesini düzenlemek için
1. İçinde **Çözüm Gezgini**, veri kümesine çift tıklayın (**.xsd** dosya) düzenlemek istediğiniz bağlantı vardır.
1. Seçin **TableAdapter** veya sorguyu düzenlemek istediğiniz bağlantısı vardır.
1. İçinde **özellikleri** penceresini genişletin **bağlantı düğümü**.
1. Hızlı bir şekilde bağlantı dizesini değiştirmek için Düzenle **ConnectionString** özelliği veya aşağı oka tıkladığınızda **bağlantı** özelliği ve **yeni bağlantı**.

## <a name="security"></a>Güvenlik
Depolama bağlantı dizesi içindeki hassas bilgileri (parola gibi), uygulamanızın güvenliğini etkileyebilir. Windows tümleşik güvenlik'i kullanarak bir veritabanına erişimi denetlemek için daha güvenli bir yoludur.
Daha fazla bilgi için [bağlantı bilgilerini koruma](/dotnet/framework/data/adonet/protecting-connection-information).

## <a name="see-also"></a>Ayrıca bkz.

- [Bağlantılar ekleme](../data-tools/add-new-connections.md)