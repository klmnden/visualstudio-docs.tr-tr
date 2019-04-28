---
title: Kullanarak yalıtılmış Kabuğu değiştirme. Pkgundef dosya | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- Visual Studio shell, isolated mode%2C .pkgundef file
ms.assetid: 9cee2a20-f8ac-4d9d-aef9-068fcd9f27a4
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: eab02fe900e96ba37c63faae535974788f99ba78
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62538400"
---
# <a name="modifying-the-isolated-shell-by-using-the-pkgundef-file"></a>Kullanarak yalıtılmış Kabuğu değiştirme. Pkgundef dosyası
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yalıtılmış Kabuk uygulaması belirtilen kayıt defteri girişlerini dışarıda bırakmak için .pkgundef dosyası değiştirebilirsiniz. Genellikle, bir bilgisayarda, bir uygulama başlatıldığında ilk kez uygulamanın kök kayıt defteri anahtarı için Visual Studio kayıt defteri girdilerinin Visual Studio Kabuğu kopyalar. Bu, şu anda yüklü VSPackages yönelik başvuruları içerir.  
  
 Bir yalıtılmış Kabuk uygulamasından bir özel kayıt defteri girişi dışlamak için paket anahtarı giriş tarafından izlenen uygulama .pkgundef dosyası ekleyin. Yalnızca .pkgdef dosyası olduğu gibi anahtarları ve girişleri temsil edilir. diğer bir deyişle [$RootKey $] veya [$RootKey$\\*alt*] ve "*giriş*" =*değer*burada *alt* etkilemek için alt *giriş* kaldırmak için giriş ve *değer* ya da `""` veya `dword:00000000`.  
  
 Dışlanacak yalnızca kayıt defteri anahtarından birden çok girişi hariç tutmak her giriş için bir satır tarafından izlenen anahtarı bir kez listeler.  
  
 Yalıtılmış Kabuk uygulaması tüm kayıt defteri anahtarı tutmak için anahtar için uygulama .pkgundef dosyası ekleyin, ancak bu anahtar için kayıt defteri girdilerini belirtmeyin.  
  
 .Pkgundef dosyaya açıklama ekleyebilirsiniz. Tek satırlı açıklama iki eğik çizgi ilk iki karakter olmalıdır.  
  
 Örneğin, kaldırmak için **veritabanına bağlan** ve **hizmet vermemesini r Bağlan** komutlarını **Araçları** menüsünde, satırın açıklamasını kaldırın:  
  
```  
[$RootKey$\Packages\{8D8529D3-625D-4496-8354-3DAD630ECC1B}]  
```  
  
 ve satır ekleyin:  
  
```  
[$RootKey$\Packages\{198E76C1-34C0-424D-9957-B3EBD80265FB}]  
```  
  
 uygulamanın .pkgundef dosyası için.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio özelliklerinin paket GUID'leri](../extensibility/package-guids-of-visual-studio-features.md)   
 [Yalıtılmış Kabuğu Özelleştirme](../extensibility/customizing-the-isolated-shell.md)
