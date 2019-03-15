---
title: 'Hızlı Başlangıç: İlk Node.js uygulamanızı oluşturmak için Visual Studio'
description: Bu hızlı başlangıçta, Visual Studio'da Node.js uygulaması oluşturma
ms.date: 06/27/2018
ms.technology: vs-javascript
ms.topic: quickstart
ms.devlang: javascript
ms.assetid: b0e4ebed-1a01-41ef-aad1-4d8465ce5322
author: mikejo5000
ms.author: mikejo
manager: jillfra
dev_langs:
- JavaScript
ms.workload:
- nodejs
ms.openlocfilehash: 8d306436f8948d6f1d22d02984b00c2e0bc8f38f
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57867018"
---
# <a name="quickstart-use-visual-studio-to-create-your-first-nodejs-app"></a>Hızlı Başlangıç: İlk Node.js uygulamanızı oluşturmak için Visual Studio

Bu 5-10 dakikalık bir giriş Visual Studio tümleşik geliştirme ortamı (IDE), basit bir Node.js web uygulaması oluşturacaksınız. Visual Studio 2017'ı henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) ücretsiz yüklemek için sayfa.

## <a name="create-a-project"></a>Proje oluşturma

İlk olarak, bir Node.js web uygulaması projesi oluşturacaksınız.

1. LTS sürümü zaten yüklü olan bir Node.js çalışma zamanı yoksa, yükleme [Node.js](https://nodejs.org/en/download/) Web sitesi.

    Genel olarak, Visual Studio yüklü Node.js çalışma zamanı otomatik olarak algılar. Yüklü bir çalışma zamanı algılayan değil, projenizi yüklü çalışma zamanı özellikleri sayfasında başvurmak için yapılandırabilirsiniz (bir proje oluşturduğunuzda, proje düğümüne sağ tıklayın ve seçin **özellikleri**).

1. Visual Studio 2017'yi açın.

1. Üstteki menü çubuğundan seçin **dosya** > **yeni** > **proje**.

1. İçinde **yeni proje** iletişim kutusunda, sol bölmede, **JavaScript**, ardından **Node.js**. Orta bölmede seçin **boş Node.js Web uygulaması**, ardından **Tamam**.

     Görmüyorsanız **boş Node.js Web uygulaması** proje şablonu, tıklayın **açık Visual Studio yükleyicisi** sol bölmesinde bağlantıyı **yeni proje** iletişim kutusu. Visual Studio Yükleyicisi'ni başlatır. Seçin **Node.js geliştirme** iş yükü, ardından **Değiştir**.

     ![Node.js iş yükü VS yükleyicisi](../ide/media/quickstart-nodejs-workload.png)

    Seçtiğiniz sonra **boş Node.js Web uygulaması** şablonu ve tıklatın **Tamam**, Visual Studio oluşturur ve yeni çözüm ve proje açılır. *Server.js* sol bölmede Düzenleyicisi'nde açılır.

## <a name="explore-the-ide"></a>IDE'yi keşfedin

1. Bir göz atın **Çözüm Gezgini** sağ bölmede.

   ![Çözüm Gezgini](../ide/media/quickstart-nodejs-solution-explorer.png)

   - Kalın yazı tipinde vurgulanmış olduğu içinde verdiğiniz ad kullanarak projenize **yeni proje** iletişim kutusu. Disk üzerinde bu proje tarafından temsil edilen bir *.njsproj* proje klasörünüzdeki dosya.

   - En üst düzeyinde ve proje ile aynı ada sahip varsayılan bir çözümdür. Tarafından temsil edilen bir çözüm, bir *.sln* dosya diskte, bir veya daha fazla ilgili proje için bir kapsayıcıdır.

   - Npm düğüm, tüm yüklü npm paketlerini gösterir. İçin arama yapın ve iletişim kutusunu kullanarak npm paketlerini yüklemek için npm düğümünü sağ tıklayabilirsiniz.

1. Npm paketlerini veya Node.js komutlar bir komut istemi'nden yüklemek istiyorsanız, proje düğümüne sağ tıklayın ve seçin **burada açık komut istemi**.

   ![Node.js komut istemi](../ide/media/quickstart-nodejs-command-prompt.png)

1. İçinde *server.js* dosya düzenleyicide (sol bölmede) öğesini `http.createServer` ve tuşuna **F12** veya tercih **tanıma** (sağ tıklama) bağlam menüsünden. Bu komut tanımına alan `createServer` işlevi *index.d.ts*.

   ![Tanıma Git bağlam menüsü](../ide/media/quickstart-nodejs-gotodefinition.png)

1. İçin geri alındı *server.js*, ardından kod, bu satırda imlecinizi dizenin sonunda put `res.end('Hello World\n');`ve şuna benzer şekilde değiştirin:

    `res.end('Hello World\n' + res.connection.`

    Girebileceğiniz `connection.`, IntelliSense, kod girişini otomatik tamamlama seçenekleri sağlar.

   ![IntelliSense otomatik tamamlama](../ide/media/quickstart-nodejs-intellisense.png)

1. Seçin **yerel bağlantı noktası**, Anahtar'a tıklayın ve `);` deyim şu şekilde görünür, böylece tamamlamak için:

    `res.end('Hello World\n' + res.connection.localPort);`

## <a name="run-the-application"></a>Uygulamayı çalıştırma

1. Tuşuna **Ctrl**+**F5** (veya **hata ayıklama > hata ayıklama olmadan Başlat**) uygulamayı çalıştırın. Uygulama bir tarayıcıda açılır.

1. Tarayıcı penceresinde "Hello World" yanı sıra yerel bağlantı noktası numarasını görürsünüz.

1. Web tarayıcısını kapatın.

Visual Studio IDE ve Node.js ile başlatıldı, bu hızlı başlangıcı tamamladığınızda tebrikler. Bir öğreticide özelliklerini daha ayrıntılı olarak inceleyin istiyorsanız, devam **öğreticiler** İçindekiler bölümünde.

## <a name="next-steps"></a>Sonraki adımlar

> [!div class="nextstepaction"]
> [Uygulamayı Linux App Service'e dağıtma](../javascript/publish-nodejs-app-azure.md)

- [Öğretici için Node.js ve Express](../javascript/tutorial-nodejs.md)
- [Node.js ve React öğretici](../javascript/tutorial-nodejs-with-react-and-jsx.md)