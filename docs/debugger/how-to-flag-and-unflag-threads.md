---
title: 'Nasıl yapılır: İş parçacıklarını bayrakla işaretleme ve bayrak | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- treads, switching [debugging]
ms.assetid: 952d579d-6911-413e-b3e5-54e7e797e70c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e63f081ff54a18bb4b5ca5c1cbdf947670f10a7e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62906731"
---
# <a name="how-to-flag-and-unflag-threads-c-visual-basic-c"></a>Nasıl yapılır: İş parçacıklarını bayrakla işaretleme ve bayrak (C#, Visual Basic, C++)

Bir simge ile işaretleyerek özel dikkat vermek istediğiniz bir iş parçacığı işaretleyebilirsiniz **iş parçacıkları**, **Paralel Yığınlar** (iş parçacığı görünümü), **paralel izleme**ve  **GPU iş parçacıkları** windows. Başkalarının bayraklı iş parçacıklarını diğer iş parçacıklarından ayırt etmek ve bu simgeyi yardımcı olabilir.

Bayraklı iş parçacıklarını ayrıca Al, özel olarak değerlendirilmesi **iş parçacığı** listesini **hata ayıklama konumu** araç ve diğer çok iş parçacıklı hata ayıklama Windows. Tüm iş parçacıkları veya yalnızca bayraklı iş parçacıklarını Göster **iş parçacığı** listesi veya diğer Windows.

### <a name="to-flag-or-unflag-a-thread"></a>Bir iş parçacığını işaretleme veya işaretini kaldırma için

- İçinde **iş parçacıkları** veya **paralel izleme** penceresinde ilgilendiğiniz iş parçacığı bulup seçmek veya bayrağını temizlemek için bayrak simgesine tıklayın.
- İçinde **Paralel Yığınlar** penceresinde, bir iş parçacığı veya grup seçin ve iş parçacıkları üzerinde sağ tıklatın **bayrağı / \<iş parçacığı >** veya **Unflag / \<iş parçacığı >**.

### <a name="to-unflag-all-threads"></a>İçin tüm iş parçacıklarının işaretini kaldır

- İçinde **iş parçacıkları** penceresinde herhangi bir iş parçacığı sağ tıklayın ve ardından **tüm iş parçacıklarını bayrakla**.
- İçinde **paralel izleme** penceresinde tüm bayraklı iş parçacıklarını, sonra sağ tıklayıp **Unflag**.

### <a name="to-display-only-flagged-threads"></a>Yalnızca bayraklı iş parçacıklarını görüntülemek için

- Seçin **sadece iş parçacığı bayrak eklenmiş Göster** bir çok iş parçacıklı hata ayıklama windows düğme.

### <a name="to-flag-just-my-code"></a>Bayrak yalnızca kendi kodum

1. Üst kısmındaki araç çubuğunda **iş parçacıkları** penceresi, bayrak simgesine tıklayın.

2. Aşağı açılan listesinde, tıklayın **bayrağı yalnızca benim kodum**.

### <a name="to-flag-threads-that-are-associated-with-selected-modules"></a>Seçili modüller ile ilişkili iş parçacıklarını için

1. Araç çubuğunda **iş parçacıkları** penceresi, bayrak simgesine tıklayın.

2. Aşağı açılan listesinde, tıklayın **bayrak Özel Modül Seçimi**.

3. İçinde **modülleri seçin** iletişim kutusunda, istediğiniz modülleri seçin.

4. (İsteğe bağlı) İçinde **arama** belirli modüller için aranacak bir dize olarak yazın.

5. **Tamam**'ı tıklatın.

## <a name="see-also"></a>Ayrıca Bkz.
- [Çok İş Parçacıklı Uygulamaların Hatalarını Ayıklama](../debugger/debug-multithreaded-applications-in-visual-studio.md)
- [Çok iş parçacıklı uygulamalarda hata ayıklamaya başlama](../debugger/get-started-debugging-multithreaded-apps.md)
- [İzlenecek yol: İş parçacıkları penceresini kullanarak birden çok iş parçacıklı uygulamalarda hata ayıklama](../debugger/how-to-use-the-threads-window.md)