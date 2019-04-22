---
title: Sözde değişken | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Watch window, pseudovariables
- debugging [Visual Studio], pseudovariables
- pseudovariables
ms.assetid: fae84f68-2138-4144-9bd4-c9e271b6182a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: dbfd275625e949e87e2b4109e1d56eaeaf9d7e3c
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59366854"
---
# <a name="pseudovariables-in-the-visual-studio-debugger"></a>Visual Studio Hata Ayıklayıcısı'sözde değişken
Sözde değişkenler, bir değişken penceresinde belirli bilgileri görüntülemek için kullanılan terimler veya **QuickWatch** iletişim kutusu. Normal bir değişken girebilirsiniz aynı şekilde sahte girebilirsiniz. Sözde değişken değil değişkenler, ancak ve programınızdaki değişken adlarına karşılık gelmez.

## <a name="example"></a>Örnek
 Yerel kod uygulaması yazdığınızı ve uygulamanızda ayrılan işleyicilerin sayısını görmek istediğinizi varsayalım. İçinde **Watch** penceresinde, aşağıdaki sözde değişkeni girebilirsiniz **adı** sütun sonra onu değerlendirmek için Return tuşuna basın:

`$handles`

 Yerel kodda aşağıdaki tabloda gösterilen pseudovariables'ı kullanabilirsiniz:

|Sözde değişkeni|İşlev|
|--------------------|--------------|
|`$err`|Ayarlama SetLastError işleviyle son hata değeri görüntüler. Görüntülenen değer GetLastError işlevi tarafından döndürülecek temsil eder.<br /><br /> Kullanım `$err,hr` bu değerin kodu çözülmüş biçimini görmek için. Örneğin, son hata 3 ise `$err,hr` görüntüler `ERROR_PATH_NOT_FOUND : The system cannot find the path specified.`|
|`$handles`|Uygulamanızda ayrılan işleyicilerin sayısını görüntüler.|
|`$vframe`|Geçerli yığın çerçevesi adresini görüntüler.|
|`$tid`|Geçerli iş parçacığı için iş parçacığı Kimliğini görüntüler.|
|`$env`|Dize Görüntüleyicisindeki ortam bloğunu görüntüler.|
|`$cmdline`|Programı başlatan komut satırı dizesini görüntüler.|
|`$pid`|İşlem kimliğini görüntüler.|
|`$` *RegisterName*<br /><br /> veya<br /><br /> `@` *RegisterName*|Kaydının içeriğini görüntüler *registername*.<br /><br /> Normalde, sadece kayıt adı girerek kayıt içeriğini görüntüleyebilirsiniz. Bu sözdizimini kullanmanız gereken yalnızca bir kez, kayıt adı bir değişken adını tekrar yüklediği zamandır. Kayıt adı geçerli kapsamdaki bir değişken adı ile aynı olduğunda, hata ayıklayıcı adı bir değişken adı olarak yorumlar. Bu durumda `$` *registername* veya `@` *registername* faydalı olur.|
|`$clk`|Saat döngüsünde zamanı görüntüler.|
|`$user`|Uygulamayı çalıştıran hesap için hesap bilgileriyle bir yapıyı görüntüler. Güvenlik nedeniyle parola bilgisi görüntülenmez.|
|`$exceptionstack`|Geçerli Windows çalışma zamanı özel durum yığın izleme görüntüler. `$ exceptionstack` UWP uygulamalarında çalışır. `$ exceptionstack` C++ ve SEH özel durumları için desteklenmiyor|
|`$returnvalue`|.NET Framework yöntemi dönüş değerini görüntüler.|

 İçinde C# aşağıdaki tabloda gösterilen pseudovariables'ı kullanabilirsiniz:

|Sözde değişkeni|İşlev|
|--------------------|--------------|
|`$exception`|Son özel durum bilgilerini görüntüler. Hiçbir özel durum oluştuysa, değerlendirme `$exception` bir hata iletisi görüntüler.<br /><br /> Özel durum Yardımcısı'nı devre dışı bırakıldığında `$exception` otomatik olarak eklenir **Yereller** bir özel durum oluştuğunda penceresi.|
|`$user`|Uygulamayı çalıştıran hesap için hesap bilgileriyle bir yapıyı görüntüler. Güvenlik nedeniyle parola bilgisi görüntülenmez.|
|`$returnvalue`|.NET Framework yöntemi dönüş değerini görüntüler.|

 Visual Basic'te, aşağıdaki tabloda gösterilen pseudovariables'ı kullanabilirsiniz:

|Sözde değişkeni|İşlev|
|--------------------|--------------|
|`$exception`|Son özel durum bilgilerini görüntüler. Hiçbir özel durum oluştuysa, değerlendirme `$exception` bir hata iletisi görüntüler.|
|`$delete` veya `$$delete`|Oluşturulan örtük değişkeni siler **hemen** penceresi. Söz dizimi `$delete,` *değişkeni* veya`$delete,` *değişkeni*`.`|
|`$objectids` veya `$listobjectids`|Tüm etkin nesne Kimlikleri'ni belirtilen ifadenin alt öğesi olarak görüntüler. Söz dizimi `$objectid,` *ifade* veya`$listobjectids,` *ifadesi*`.`|
|`$` *N* `#`|Eşit nesne Kimliğine sahip nesneyi görüntüler *N*.|
|`$dynamic`|Özel görüntüler **dinamik Görünüm** uygulayan bir nesne düğümü `IDynamicMetaObjectProvider`. Arabirim. Söz dizimi `$dynamic,` *nesne*. Bu özellik yalnızca .NET Framework sürüm 4 kullanan kod için geçerlidir.|

## <a name="see-also"></a>Ayrıca Bkz.
- [İzleme ve Hızlı İzleme Pencereleri](../debugger/watch-and-quickwatch-windows.md)
- [Değişken Windows](../debugger/debugger-windows.md)
