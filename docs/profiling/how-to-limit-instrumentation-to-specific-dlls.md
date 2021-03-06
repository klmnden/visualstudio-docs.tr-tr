---
title: "Nasıl yapılır: Belirli DLL'ler için izleme sınırlama | Microsoft Docs"
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- performance tools, runtime profiling control window
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b39689219b113343162aa0e814cfa68e2422f08d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62980921"
---
# <a name="how-to-limit-instrumentation-to-specific-dlls"></a>Nasıl yapılır: İzlemeyi belirli DLL'ler ile sınırlama

İzleme profil oluşturma metodunu kullanarak bir uygulama bir veya daha fazla dll için profil oluşturma verilerinin toplanmasını sınırlayabilirsiniz. Bir uygulama bir veya daha fazla dll profil için içeren bir performans oturumu oluşturun. *dll* hedefleri olarak dosyaları. Projeleri Visual Studio çözümünde veya bağımsız ikili dosyaları olarak profil oluşturmak istediğiniz DLL'leri belirtebilirsiniz.

## <a name="to-limit-instrumentation-to-specific-dlls-in-a-visual-studio-solution"></a>Visual Studio çözümünde belirli DLL'ler için izleme sınırlama

1. Visual Studio'da DLL içeren çözümü açın.

2. Üzerinde **Çözümle** menüsünde **performans Sihirbazını Başlat**.

3. Seçin **izleme** 'a tıklayın ve profil oluşturma yöntemi olarak **sonraki**.

4. Gelen **aşağıdaki kullanılabilir hedeflerden hangisi için profil ister misiniz?**, adını seçin. *dll* proje ve ardından **sonraki**.

5. Tıklayın **son** sihirbazdan çıkın ve yeni performans oturumu görüntülemek için **performans Gezgini** penceresi.

6. Sağ **hedefleri** seçip **hedef Proje Ekle**.

7. Gelen **hedef Proje Ekle** listesinde, DLL kullanmak için kullanmak istediğiniz yürütülebilir projeyi seçin.

     İsteğe bağlı. İstediğiniz herhangi bir DLL projelerinde profiline ekleyebilirsiniz.

8. Eklenen bir proje için veri toplama önlemek için proje adına sağ tıklayın ve ardından temizleyin **gereç** onay kutusu.

## <a name="to-specify-specific-dlls-to-profile-as-independent-binaries"></a>Profil için belirli DLL'ler bağımsız ikili dosyaları belirtmek için

1. Visual Studio'yu açın.

2. Üzerinde **Çözümle** menüsünde **performans Sihirbazını Başlat**.

3. Gelen **aşağıdaki kullanılabilir hedeflerden hangisi için profil istediğiniz**seçin **bir dinamik bağlantı kitaplığı profili (. DLL)** ve ardından **sonraki**.

4. Sihirbazın ikinci sayfasında, aşağıdaki adımları gerçekleştirin:

    - Yol ve dosya adını yazın. *dll* profilinde istediğiniz dosya **Dll yolu**. Dosyayı bulmak için üç nokta düğmesini (…) de tıklatabilirsiniz **dinamik bağlantı kitaplığı profili** iletişim kutusu. Kopyasını belirtmeniz gerektiğini unutmayın. *dll* yürütülebilir dosya tarafından başlatılan bir dosya (. *exe*), ardından seçtiğiniz dosya.

    - Yürütülebilir dosya yolu ve dosya adını yazın (. *exe*) çalışma bir dosya. *dll* içinde **yürütülebilir dosya yolu**. Dosyayı bulmak için üç nokta düğmesini (…) de tıklatabilirsiniz **başlatılacak yürütülebilir** iletişim kutusu.

    - İsteğe bağlı. Yürütülebilir dosyaya geçirilecek istediğiniz komut satırı bağımsız değişkenleri girin **komut satırı bağımsız değişkenleri**. Gerekirse, uygulama için çalışma dizini belirtin **çalışma dizini**.

    - **İleri**'ye tıklayın.

5. Seçin **izleme** 'a tıklayın ve profil oluşturma yöntemi olarak **sonraki**.

6. Tıklayın **son** sihirbazdan çıkın ve yeni performans oturumu görüntülemek için **performans Gezgini** penceresi.

7. İsteğe bağlı. Daha fazla eklemek için. *dll* dosyalarını, sağ **hedefleri** seçip **hedef ikili Ekle**. Dosyaları Seç **hedef ikili Ekle** iletişim kutusu.

    > [!NOTE]
    > Yürütülebilir dosyayı belirtmeyin (. *exe*) DLL'leri sınayan dosya.

## <a name="see-also"></a>Ayrıca bkz.

[Veri toplamayı kontrol](../profiling/controlling-data-collection.md)
[nasıl yapılır: Belirli işlevler için izlemeyi sınırı](../profiling/how-to-limit-instrumentation-to-specific-functions.md)