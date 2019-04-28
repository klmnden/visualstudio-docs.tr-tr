---
title: 'Nasıl yapılır: Belirli işlevlere izlemeyi sınırlama | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- performance tools, limiting instrumentation to functions
ms.assetid: bd98d6bf-2560-4eba-b063-2facb09f87c4
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 826031c2030c2ed8662ff98517a36c1a7ade3cde
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63386643"
---
# <a name="how-to-limit-instrumentation-to-specific-functions"></a>Nasıl yapılır: İzlemeyi belirli araçlarla sınırlama
Bir veya daha fazla işlev için izleme ve veri toplama seçeneklerini ayarlayarak sınırlayabilirsiniz **Gelişmiş** sayfasının **performans oturumu** veya hedef ikili özellik sayfaları:

- Performans oturumu özelliği sayfasında işlevleri belirtirseniz, bu işlevler yalnızca oturumun tüm izleme eklenmiş ikili dosyalarda algılayıcılarla donatılmıştır.

- İkili bir hedef özellik sayfasında işlevleri belirtirseniz, belirli bir ikili izleme eklenmiş, bu işlevler yalnızca bu şekilde çalışır. Diğer ikili performans işlevlerde zamanki algılayıcılarla donatılmıştır.

  Yalnızca izleme profili oluşturma metodu seçildiğinde, bu şekilde veri toplama sınırlaması desteklenir.

> [!NOTE]
> Ayrıca **Gelişmiş** sayfasının **performans oturumu** profil oluşturma araçları için kullanılabilir diğer seçenekleri ayarlamak için özellik sayfaları [Vsınstr](../profiling/vsinstr.md) komut satırı izleme aracı.

### <a name="to-limit-instrumentation-to-specific-functions-in-a-performance-session"></a>Performans oturumu içinde belirli işlevler için izlemeyi sınırlama

1. İçinde **performans Gezgini**oturum adına sağ tıklayın ve ardından **özellikleri**.

    **Özellik sayfaları** iletişim kutusu görüntülenir.

2. Üzerinde **özellik sayfaları** iletişim kutusu, tıklayın **Gelişmiş**.

3. İçinde **ek izleme seçeneklerini** metin kutusunda, istediğiniz işlev adı türü için aşağıdaki sözdizimini kullanın. aracı:

    **/ include:** `FuncSpec` **[;** `FuncSpec` **]** `...`

    `FuncSpec` ad alanı ve işlev adıdır. Şu biçimdedir `Namespace` **::**`FunctionName`. Birden çok işlevleri ayırmak için noktalı virgül kullanın. Bir yıldız işareti kullanın (\*) bir veya daha fazla karakter için joker karakter belirtmek için. Örneğin, **/ include: MyNS::\\*** MyNS ad alanındaki tüm işlevleri belirtir.

   > [!NOTE]
   > Bir ikili işlevlerde listelemek için profil oluşturma araçları yükleme dizininde bir komut istemi penceresi açın (bkz [komut satırı araçları yolunu belirtin](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md)) ve ardından yazın **vsınstr /DumpFuncs**

### <a name="to-limit-instrumentation-to-specific-functions-in-a-binary"></a>Bir ikili dosyada belirli işlevler için izlemeyi sınırlama

1. İçinde **performans Gezgini**, ikili adı bulun **hedefleri** performans oturumu düğümünün.

2. İkili adına sağ tıklayın ve ardından **özellikleri**.

    **Özellik sayfaları** iletişim kutusu görüntülenir.

3. Üzerinde **özellik sayfaları** iletişim kutusu, tıklayın **Gelişmiş**.

4. İçinde **ek izleme seçeneklerini** metin kutusunda, istediğiniz işlev adı türü için aşağıdaki sözdizimini kullanın. aracı:

    **/ include:** `FuncSpec` **[;** `FuncSpec` **]** `...`

    `FuncSpec` ad alanı ve işlev adıdır. Şu biçimdedir `Namespace` **::**`FunctionName`. Birden çok işlevleri ayırmak için noktalı virgül kullanın. Bir yıldız işareti kullanın (\*) bir veya daha fazla karakter için joker karakter belirtmek için. Örneğin, **/ include: MyNS::\\*** MyNS ad alanındaki tüm işlevleri belirtir.

   > [!NOTE]
   > Bir ikili işlevlerde listelemek için profil oluşturma araçları yükleme dizininde bir komut istemi penceresi açın (bkz [komut satırı araçları yolunu belirtin](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md)) ve ardından yazın **vsınstr /DumpFuncs**

## <a name="see-also"></a>Ayrıca bkz.
- [Veri toplamayı denetleme](../profiling/controlling-data-collection.md)
- [Nasıl yapılır: Sınırı izlemeyi belirli DLL'ler](../profiling/how-to-limit-instrumentation-to-specific-dlls.md)
- [Nasıl yapılır: Ek izleme seçeneklerini belirtme](../profiling/how-to-specify-additional-instrumentation-options.md)