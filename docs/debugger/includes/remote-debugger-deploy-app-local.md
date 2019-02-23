---
title: Yerel klasöre dağıtma
description: Uygulama bir yerel klasöre dağıtma
services: ''
author: mikejo5000
ms.service: ''
ms.topic: include
ms.date: 05/23/2018
ms.author: mikejo
ms.custom: include file
ms.openlocfilehash: 67ffd17c772221c356e8c25d14437c2a737fda9e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56723883"
---
1. İçinde **Çözüm Gezgini**, proje düğümüne sağ tıklayıp **Yayımla** (Web formları için **Web uygulaması yayımlama**).

    Tüm yayımlama profilleri, daha önce yapılandırdıysanız **Yayımla** bölmesi görünür. Tıklayın **yeni profili**.

1. İçinde **Yayımla** iletişim kutusunda **klasör**, tıklayın **Gözat**ve yeni bir klasör oluşturun **C:\Publish**.

    ![RemoteDBG_Publish_Local](../media/remotedbg_publish_local.png "RemoteDBG_Publish_Local")

    Bir Web Forms uygulaması için seçin **özel** Yayımla iletişim kutusunda, bir profil adı girin ve seçin **Tamam**.

1. Tıklayın **profili oluşturma** aşağı açılan listesinde (**Yayımla** varsayılan değerdir).

1. İçinde **Yayımla** iletişim kutusu, tıklayın **ayarları** bağlantısını ve ardından **ayarları** sekmesi.

1. Yapılandırmayı ayarlamak **hata ayıklama**seçin **var olan tüm dosyaları yayımlama öncesi silme**ve ardından **Kaydet**.

    > [!NOTE]
    > Yayın derlemesi kullanırsanız, yayımladığınızda, web.config dosyasında hata ayıklamayı devre dışı.

1. Tıklayın **yayımlama**.

    ![RemoteDBG_Publish_Debug_Config](../media/remotedbg_publish_debug_config.png "RemoteDBG_Publish_Debug_Config")

    Uygulamanın yayınlar bir **hata ayıklama** yerel klasörde proje yapılandırması. Çıkış penceresinde ilerleme durumunu gösterir.

1. ASP.NET proje dizini Visual Studio bilgisayarı ASP.NET uygulaması için yapılandırılan yerel dizine kopyalayın (Bu örnekte, **C:\Publish**) Windows Server bilgisayarında. Bu öğreticide, el ile kopyalama ve PowerShell, Xcopy veya Robocopy gibi diğer araçları kullanabilirsiniz varsayıyoruz.

    > [!CAUTION]
    >  Kod veya yeniden oluşturma için değişiklikler yapmanız gerekirse yeniden yayımlamanız ve bu adımı yineleyin. Yerel kaynak ve simgeler, uzak makineye kopyaladığınız yürütülebilir dosyanın tam olarak eşleşmelidir.    Bu alırsınız gerçekleştirmezseniz bir `cannot find or open the PDB file` Visual Studio'da hata ayıklama işlemini denediğinizde uyarı.

1. Windows Server'da, uygulamanın doğru şekilde uygulamayı tarayıcınızda açarak çalıştırabildiğinizi doğrulayın.

    Uygulamayı doğru şekilde çalışmazsa, ASP.NET sunucunuz hem de Visual Studio makinenizde yüklü sürümü arasında bir uyuşmazlık olabilir ya da IIS veya Web sitesi yapılandırma ile bir sorun olabilir. Önceki adımları yeniden denetleyin.
