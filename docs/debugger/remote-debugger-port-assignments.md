---
title: Uzaktan hata ayıklayıcı bağlantı noktası atamaları | Microsoft Docs
ms.custom: ''
ms.date: 05/18/2018
ms.topic: reference
ms.assetid: 238bb4ec-bb00-4c2b-986e-18ac278f3959
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e65ea21e0b1e7c7f4e8899410c0c3b454e0630e3
ms.sourcegitcommit: 3ca33862c1cfc3ccb83de3e95f1e69e860ab143a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57526149"
---
# <a name="remote-debugger-port-assignments"></a>Uzaktan hata ayıklayıcı bağlantı noktası atamaları
Visual Studio uzaktan hata ayıklayıcı, bir uygulama veya bir arka plan hizmeti olarak çalıştırabilirsiniz. Bir uygulama olarak yürütüldüğünde, varsayılan olarak şu şekilde atanan bir bağlantı noktası kullanır:
::: moniker range=">=vs-2019"
- Visual Studio 2019: 4024
::: moniker-end
- Visual Studio 2017: 4022

- Visual Studio 2015: 4020

- Visual Studio 2013 için: 4018

- Visual Studio 2012 için: 4016

  Diğer bir deyişle, her sürüm için 2 tarafından uzaktan hata ayıklayıcı için atanan bağlantı noktası numarası artırılır. Farklı bir bağlantı noktası numarası gibi ayarlayabilirsiniz. Şu bağlantı noktası numaraları daha sonraki bir bölümde ayarlama açıklanmaktadır.

## <a name="the-remote-debugger-port-on-32-bit-operating-systems"></a>32 bit işletim sistemlerinde uzaktan hata ayıklayıcı bağlantı noktası

::: moniker range=">=vs-2019"
 (Visual Studio 2019) gelen TCP 4024 ana bağlantı noktası ve tüm senaryolar için gereklidir. Bu komut satırı veya uzaktan hata ayıklayıcı penceresinde yapılandırabilirsiniz.
::: moniker-end
::: moniker range="vs-2017"
 TCP 4022 (Visual Studio 2017), ana bağlantı noktası ve tüm senaryolar için gereklidir. Bu komut satırı veya uzaktan hata ayıklayıcı penceresinde yapılandırabilirsiniz.
::: moniker-end

 Uzaktan hata ayıklayıcı penceresinde **Araçlar > Seçenekler**, TCP/IP bağlantı noktası numarasını ayarlayın.

 Uzaktan hata ayıklayıcı ile komut satırında başlatmak **/bağlantı noktası** geçiş: **msvsmon/Port \<bağlantı noktası numarası >**.

 Komut satırı anahtarları hata ayıklama Uzaktan Yardım'daki tüm uzaktan hata ayıklayıcıyı bulabilirsiniz (basın **F1** veya **Yardım > kullanım** uzaktan hata ayıklayıcı penceresinde).

## <a name="the-remote-debugger-port-on-64-bit-operating-systems"></a>64-bit işletim sistemlerinde uzaktan hata ayıklayıcı bağlantı noktası
::: moniker range=">=vs-2019"
 Uzaktan hata ayıklayıcı 64-bit sürümünü başlatıldığında, ana kullanır (4024) varsayılan olarak bağlantı noktası.  Bir 32 bit işlemde hata ayıklamak, uzaktan hata ayıklayıcı 64-bit sürümü 32 bit sürümü (ana bağlantı noktası numarası 1 ile artan) uzaktan hata ayıklayıcı bağlantı noktası 4025 başlatır. 32-bit uzaktan hata ayıklayıcı çalıştırırsanız, 4024 kullanır ve 4025 kullanılmaz.
::: moniker-end
::: moniker range="vs-2017"
 Uzaktan hata ayıklayıcı 64-bit sürümünü başlatıldığında, ana kullanır (4022) varsayılan olarak bağlantı noktası.  Bir 32 bit işlemde hata ayıklamak, uzaktan hata ayıklayıcı 64-bit sürümü 32 bit sürümü (ana bağlantı noktası numarası 1 ile artan) uzaktan hata ayıklayıcı 4023 bağlantı noktasında başlatır. 32-bit uzaktan hata ayıklayıcı çalıştırırsanız, 4022 kullanır ve 4023 kullanılmadığı.
:::moniker-end

 Bu bağlantı noktası, komut satırından yapılandırılabilir: **Msvsmon/wow64port \<bağlantı noktası numarası >**.

## <a name="the-discovery-port"></a>Bulma bağlantı noktası
 UDP 3702, ağ üzerinde çalışan uzaktan hata ayıklayıcı örneklerini bulmak için kullanılır (örneğin, **Bul** iletişim kutusunda **iliştirme** iletişim). Yalnızca makine adı veya IP adresi hedef bilgisayarın olduğunu bilmesinin başka bir şekilde varsa isteğe bağlı, bu nedenle uzaktan hata ayıklayıcı, çalışan bir makine bulmak için kullanılır. Bağlantı noktası numarası yapılandırılamaz için bu bulma, standart bir bağlantı noktasıdır.

 Bulmayı etkinleştirmek istemiyorsanız, devre dışı keşif ile komut satırından msvsmon başlatabilirsiniz:  **Msvsmon /nodiscovery**.

## <a name="remote-debugger-ports-on-azure"></a>Azure uzaktan hata ayıklayıcı bağlantı noktaları
 Aşağıdaki bağlantı noktaları, Azure üzerinde uzaktan hata ayıklayıcı tarafından kullanılır. Bulut hizmeti bağlantı noktalarını tek tek bir VM üzerindeki bağlantı noktalarına eşlenir. TCP tüm bağlantı noktaları şunlardır.

|Bağlantı|Bulut hizmeti bağlantı noktası|VM üzerindeki bağlantı noktası|
|-|-|-|
|Microsoft.WindowsAzure.Plugins.RemoteDebugger.Connector|30400|30398|
|Microsoft.WindowsAzure.Plugins.RemoteDebugger.Forwarder|31400|31398|
|Microsoft.WindowsAzure.Plugins.RemoteDebugger.FileUpload|32400|32398|

## <a name="see-also"></a>Ayrıca Bkz.
- [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)