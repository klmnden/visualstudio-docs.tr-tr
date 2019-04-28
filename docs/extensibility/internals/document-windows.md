---
title: Windows belge | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Visual Studio SDK, document windows
ms.assetid: 50081d48-987f-43db-8bf9-51b7cf76e9c0
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 490c39b9e97ad6a55ca2d1695d31b85ecc13dc57
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63418591"
---
# <a name="document-windows"></a>Belge pencereleri
Visual Studio'da bir *belge penceresi* bir çok Belgeli Arabirim (MDI) penceresi ile ilişkili bir Çerçeveli alt penceredir. Belge pencereleri genellikle görüntüleme ve kaynak kodu veya metin değişikliği için kullanılır, ancak işlev diğer türleri de barındırabilir. Belge pencereleri:

- Böylece birden çok dosyayı aynı anda görüntülenebilir, üst MDI ayrı yatay veya dikey sekme grupları içinde düzenlenebilir.

- MDI üst herhangi bir sırada sabitlenebilir.

- Özgürce kaydırıldı.

- Diğer MDI pencereleri için sekmesinde sırayla bağlanır.

  Komutları gruplandırma için yerleşen ve kayan bir belge penceresi sekme kısayol menüsünde bulunabilir.

  Visual Studio'da pencere davranış hakkında daha fazla bilgi için bkz. [pencere düzenlerini özelleştirme](../../ide/customizing-window-layouts-in-visual-studio.md).

## <a name="document-window-implementation"></a>Belge penceresi uygulama
 Belge pencereleri, bir düzenleyici uygulayarak oluşturulur. <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory> Arabirimi bir düzenleyici örnekleme bir parçası olarak belge pencerelerini oluşturur. Daha fazla bilgi için [eski arabirimleri Düzenleyicisi'nde](../../extensibility/legacy-interfaces-in-the-editor.md).

> [!NOTE]
> Geriye doğru sağlamak ve bir pencere gezinti noktaları iletmek üzere uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsBackForwardNavigation> arabirimi. Metin Düzenleyicisi metin işaretçileri belgedeki Gezinti noktalarını tanımlamak için kullanır.

## <a name="the-running-document-table"></a>Çalıştırılan Belge tablosu
 IDE her belge penceresi durumunu izlemek için çalıştırılan Belge tablosu (RDT) kullanır. RDT hangi belge windows olaylarını gibi bir çözüm kapatıldığında veya bir dosya düzenlendiğinde, bildirilir mekanizmadır. Daha fazla bilgi için [çalıştırılan Belge tablosu](../../extensibility/internals/running-document-table.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Gecikmeli belge yüklemesi](../../extensibility/internals/delayed-document-loading.md)