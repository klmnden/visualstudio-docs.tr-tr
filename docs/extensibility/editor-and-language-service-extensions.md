---
title: Düzenleyici ve dil hizmeti uzantıları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK]
ms.assetid: 5653bac9-724f-4948-a820-68ce6aa96365
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1df6f65db70425650fc2860bf5ddf6e2d2e203c6
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66353377"
---
# <a name="editor-and-language-service-extensions"></a>Düzenleyici ve dil hizmeti uzantıları
Çoğu Visual Studio Kod Düzenleyicisi özelliklerini genişletebilirsiniz. Düzenleyici, Windows Presentation Foundation (WPF) dayanır ve yönetilen kodda yazılır. Bu tasarım, Visual Studio'nun önceki sürümlerinde tasarımları farklıdır, aynı özelliklerin çoğunu sağlar. Düzenleyiciyi genişletmek için Yönetilen Genişletilebilirlik Çerçevesi (MEF) kullanın.

 Visual Studio SDK'sı olarak da bilinen bağdaştırıcıları sağlar *dolgular* önceki sürümleri için yazılmış VSPackages desteklemek için. Bununla birlikte, mevcut bir VSPackage varsa, daha iyi performans ve güvenilirlik elde etmek için yeni teknoloji güncelleştirme öneririz.

## <a name="related-topics"></a>İlgili konular

|Başlık|Açıklama|
|-----------|-----------------|
|[Bir düzenleyici öğesi şablonuyla uzantı oluşturma](../extensibility/creating-an-extension-with-an-editor-item-template.md)|Düzenleyici öğesi şablonlarını kullanarak giriş.|
|[Düzenleyici ve dil hizmetlerini genişletme](../extensibility/extending-the-editor-and-language-services.md)|Tasarım ve çekirdek Düzenleyici özelliklerini tanıtır ve genişletmek nasıl Göster belgelere bağlantılar.|
|[Eski arabirimleri Düzenleyicisi](../extensibility/legacy-interfaces-in-the-editor.md)|Mevcut koddan çekirdek Düzenleyicisi'ne erişmek nasıl açıklayan belgelere bağlantılar.|
|[Özel düzenleyiciler ve tasarımcılar oluşturma](../extensibility/creating-custom-editors-and-designers.md)|Özel düzenleyicilerde nasıl oluşturulacağını açıklayan belgelere bağlantılar.|
|[Eski dil hizmeti genişletilebilirliği](../extensibility/internals/legacy-language-service-extensibility.md)|Programlama dilleri Visual Studio ile tümleştirmek nasıl açıklayan belgelere bağlantılar.|
|[Managed Extensibility Framework (MEF)](/dotnet/framework/mef/index)|Yönetilen Genişletilebilirlik Çerçevesi (MEF) sunar.|
|[Windows Presentation Foundation](/dotnet/framework/wpf/index)|Windows Presentation Foundation (WPF) sunar.|