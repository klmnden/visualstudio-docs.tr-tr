---
title: 'Nasıl Yapılır: Karışık modda hata ayıklama | Microsoft Docs'
ms.date: 11/05/2018
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging DLLs
- debugging [Visual Studio], mixed-mode
- mixed-mode debugging
ms.assetid: 2859067d-7fcc-46b0-a4df-8c2101500977
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: db26a3a68b15dcd6252f6bd02a540e105c993b54
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53896064"
---
# <a name="how-to-debug-in-mixed-mode-c-c-visual-basic"></a>Nasıl Yapılır: Karışık modda hata ayıklama (C#, C++, Visual Basic)

Aşağıdaki yordamlar, yönetilen ve yerel kod birlikte, olarak da bilinen karışık mod hata ayıklama için hata ayıklamayı nasıl etkinleştireceğinizi açıklar. İki karma mod hata ayıklama senaryoları şunlardır:

- Bir DLL çağıran uygulama yerel kodda yazılır ve DLL yönetilir.

- Bir DLL çağıran uygulama, yönetilen kodda yazılır ve yerel kodda DLL'dir. Bu senaryo daha ayrıntılı size bir öğretici için bkz [yönetilen ve yerel kodda hata ayıklama](../debugger/how-to-debug-managed-and-native-code.md).

Hem yönetilen hem de yerel hata ayıklayıcıları çağıran uygulama projenin etkinleştirebilirsiniz **özelliği** sayfaları. Ayarlar, yerel ve yönetilen uygulamalar arasında farklılık gösterir.

Çağıran uygulamanın projeye erişimi yoksa, DLL DLL projesinden ayıklayabilirsiniz. Karma mod yalnızca DLL proje hatalarını ayıklamaya gerekmez. Daha fazla bilgi için [nasıl yapılır: Bir DLL projesinde hata ayıklama](../debugger/how-to-debug-from-a-dll-project.md).

> [!NOTE]
> İletişim kutuları ve gördüğünüz komutları bu makalede, Visual Studio ayarları veya sürüm bağlı olarak gösterilenlerden farklı olabilir. Ayarlarınızı değiştirmek için seçin **Araçları** > **içeri ve dışarı aktarma ayarları**. Daha fazla bilgi için [ayarlarına](../ide/environment-settings.md#reset-settings).

## <a name="enable-mixed-mode-debugging-for-a-native-calling-app"></a>Yerel çağıran bir uygulama için karışık mod hata ayıklamayı etkinleştir

1. C++ projesinde seçin **Çözüm Gezgini** tıklatıp **özellikleri** simgesi, tuşuna **Alt**+**Enter**, veya sağ tıklatın ve seçin **özellikleri**.

1. İçinde  **\<Proje > özellik sayfaları** iletişim kutusunda **yapılandırma özellikleri**ve ardından **hata ayıklama**.

1. Ayarlama **hata ayıklayıcı türü** için **karma** veya **otomatik**.

1. **Tamam**’ı seçin.

   ![Karışık mod hata ayıklamayı](../debugger/media/dbg-mixed-mode-from-native.png "karışık modda hata ayıklama etkinleştirme")

## <a name="enable-mixed-mode-debugging-for-a-managed-calling-app"></a>Yönetilen çağıran bir uygulama için karışık mod hata ayıklamayı etkinleştir

1. C# veya Visual Basic projesinde seçin **Çözüm Gezgini** seçip **özellikleri** simgesi, tuşuna **Alt**+**Enter**, veya sağ tıklayıp seçin **özellikleri**.

1. Seçin **hata ayıklama** sekmesine tıklayın ve ardından **yerel kod hata ayıklamayı**.

1. Değişiklikleri kaydetmek için Özellikler sayfasını kapatın.

   ![Yerel kod hata ayıklamayı](../debugger/media/dbg-mixed-mode-from-csharp.png "yerel kod hata ayıklamayı etkinleştir")

> [!NOTE]
> Çoğu Visual Studio 2017 sürümünde kullanmalısınız *launchSettings.json* dosya yerine bir .NET Core uygulaması yerel kod için karışık mod hata ayıklamayı etkinleştirmek için proje özellikleri. Ayrıntılar için bkz [yönetilen ve yerel kodda hata ayıklama](../debugger/how-to-debug-managed-and-native-code.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Bir DLL projesinde hata ayıklama](../debugger/how-to-debug-from-a-dll-project.md)