---
title: Dış araçları yönetme
ms.date: 11/20/2017
ms.prod: visual-studio-dev15
ms.topic: conceptual
f1_keywords:
- vs.externaltools
helpviewer_keywords:
- external tools [Visual Studio]
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 8f918ad272683de5316467d1027e098c1ead91a6
ms.sourcegitcommit: 73861cd0ea92e50a3be1ad2a0ff0a7b07b057a1c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54154069"
---
# <a name="manage-external-tools"></a>Dış araçları yönetme

Dış Araçları'ndan çağırabilirsiniz kullanarak Visual Studio içinde **Araçları** menüsü. Birkaç varsayılan araç ulaşılabilir **Araçları** menü ve özelleştirme menüsünü diğer yürütülebilir dosyaların kendi ekleyerek.

## <a name="tools-available-on-the-tools-menu"></a>Araçlar menüsünde kullanılabilen Araçlar

**Araçları** menü birkaç yerleşik komutu gibi içerir:

* **Uzantılar ve güncelleştirmeler** için [Visual Studio uzantılarını yönetme](finding-and-using-visual-studio-extensions.md)
* **Kod parçacıkları Yöneticisi** için [kod parçacıkları düzenleme](code-snippets.md)
* **PreEmptive koruma - Dotfuscator** başlatmak için [Dotfuscator Community Edition'ı (CE)](dotfuscator/index.md) ise [yüklü](dotfuscator/install.md)
* **Özelleştirme** için [menüleri ve araç çubuklarını özelleştirme](how-to-customize-menus-and-toolbars-in-visual-studio.md)
* **Seçenekleri** için [çeşitli Visual Studio IDE ve diğer araçları için farklı seçenekleri ayarlama](reference/options-dialog-box-visual-studio.md)

## <a name="add-new-tools-to-the-tools-menu"></a>Araçlar menüsüne yeni araçları ekleme

Görüntülenmesini harici bir aracı ekleyebilirsiniz **Araçları** menüsü.

1. Açık **dış Araçlar** iletişim kutusunu **Araçları** > **dış Araçları**.

1. Tıklayın **Ekle**ve ardından bilgileri doldurun. Örneğin, aşağıdaki giriş neden **Windows Explorer** dosya dizininde açmak için şu anda Visual Studio'da açtığınız:

   * Başlık: `Open File Location`

   * Komut: `explorer.exe`

   * Bağımsız değişkenleri: `/root, "$(ItemDir)"`

   ![Dış araçlar iletişim kutusu](media/external-tools-dialog.png)

Dış bir araç tanımlarken kullanılabilir değişkenlerin tam listesi verilmiştir:

|Ad|Bağımsız Değişken|Açıklama|
|----------|--------------|-----------------|
|Öğe yolu|$(ItemPath)|Geçerli dosyanın tam dosya adı (sürücü yolu + dosya adı).|
|Öğe dizini|$(ItemDir)|Geçerli bir dosya (sürücü + yolu) dizini.|
|Öğe dosya adı|$(ItemFilename)|Dosya adı geçerli dosyanın (dosya adı).|
|Öğesi uzantısı|$(ItemExt)|Geçerli dosyanın dosya adı uzantısı.|
|Geçerli satırı|$(CurLine)|İmleci kod penceresinde geçerli satır konumu.|
|Geçerli sütun|$(CurCol)|İmleci kod penceresinde geçerli sütun konumu.|
|Geçerli metin|$(CurText)|Seçili metni.|
|Hedef yolu|$(TargetPath)|Oluşturulacak öğe tam dosya adı (sürücü yolu + dosya adı).|
|Hedef Dizin|$(TargetDir)|Oluşturulacak öğe dizini.|
|Hedef Adı|$(TargetName)|Oluşturulacak öğe dosya adı.|
|Hedef uzantısı|$(TargetExt)|Oluşturulacak öğesinin dosya adı uzantısı.|
|İkili dizin|$(BinDir)|Oluşturulmakta olan ikili (sürücü + yolu tanımlanan) son konum.|
|Proje dizini|$(ProjectDir)|Geçerli proje (sürücü + yolu) dizini.|
|Proje dosyası adı|$(ProjectFileName)|Geçerli projenin dosya adını (sürücü yolu + dosya adı).|
|Çözüm dizini|$(SolutionDir)|Geçerli çözüme (sürücü + yolu) dizini.|
|Çözüm dosyası adı|$(SolutionFileName)|Geçerli çözümün dosya adını (sürücü yolu + dosya adı).|

> [!NOTE]
> IDE durum çubuğu görüntüler **geçerli satırı** ve **geçerli sütunun** noktasını etkin nerede göstermek için değişkenleri **Kod Düzenleyicisi**. **Geçerli metin** metin veya bu konumda seçili kod değişkeni döndürür.

## <a name="see-also"></a>Ayrıca bkz.

- [C/C++ derleme araçları](/cpp/build/reference/c-cpp-build-tools)
