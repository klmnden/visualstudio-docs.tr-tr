---
title: "Nasıl yapılır: DLL'lerde hata ayıklama | Microsoft Docs"
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.dll
dev_langs:
- FSharp
- VB
- CSharp
- C++
- VB
- CSharp
- C++
helpviewer_keywords:
- debugging DLLs
- DLLs, debugging
- executable files, specifying for debug sessions
ms.assetid: 76b34d15-a66d-4963-842e-c8b955c81696
caps.latest.revision: 20
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 16a533b27e619526edab71374d922e68baf0a4b0
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65702673"
---
# <a name="how-to-debug-native-dlls"></a>Nasıl yapılır: DLL'lerde hata ayıklama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

> [!NOTE]
> Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir. Ayarlarınızı değiştirmek için Araçlar menüsünden içeri ve dışarı aktarma ayarları seçin. Daha fazla bilgi için [Visual Studio'da geliştirme ayarlarını özelleştirme](https://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
 Bir DLL'de hata ayıklamak, hata ayıklamayı başlayabilirsiniz:  
  
- Yürütülebilir dosyayı oluşturmak için kullanılan proje DLL çağırır.  
  
  \- veya -  
  
- DLL'yi oluşturmak için kullanılan proje.  
  
  Yürütülebilir dosyayı oluşturmak için kullanılan bir proje varsa, bu projeden hata ayıklamayı başlatın. Ardından, DLL için bir kaynak dosyasını açın ve yürütülebilir dosyayı oluşturmak için kullanılan projenin bir parçası olmasa bile, bu dosyada kesme noktaları ayarlayın. Daha fazla bilgi için [kesme noktaları](https://msdn.microsoft.com/fe4eedc1-71aa-4928-962f-0912c334d583).  
  
  DLL oluşturur projeden hata ayıklamayı başlatırsanız, hata ayıklama DLL içinde kullanmak istediğiniz yürütülebilir dosyanın belirtmeniz gerekir.  
  
### <a name="to-specify-an-executable-for-the-debug-session"></a>Hata ayıklama oturumu için yürütülebilir bir dosya belirtmek için  
  
1. İçinde **Çözüm Gezgini**, DLL oluşturur projeyi seçin.  
  
2. Gelen **görünümü** menüsünde seçin**özellik sayfaları**.  
  
3. İçinde **özellik sayfaları** açık iletişim kutusunu **yapılandırma özellikleri** klasörü ve select **hata ayıklama** kategorisi.  
  
4. İçinde **komut** kutusunda, kapsayıcı için yol adı belirtin. Örneğin, C:\Program Files\MyApplication\MYAPP. EXE.  
  
5. İçinde **komut satırı bağımsız değişkenlerini** kutusunda, yürütülebilir dosya için gerekli olan herhangi bir bağımsız değişken belirtin.  
  
   Yürütülebilir dosya belirtmezseniz _proje_**özellik sayfaları** iletişim kutusu, [hata ayıklama oturumu iletişim kutusu için yürütülebilir](../debugger/executable-for-debugging-session-dialog-box.md) hata ayıklamaya başladığınızda görünür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata ayıklayıcısı güvenliği](../debugger/debugger-security.md)   
 [Visual Studio’da hata ayıklama](../debugger/debugging-in-visual-studio.md)
