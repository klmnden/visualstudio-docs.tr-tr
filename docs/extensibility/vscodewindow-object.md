---
title: VSCodeWindow nesnesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- VSCodeWindow
helpviewer_keywords:
- views [Visual Studio SDK], VSCodeWindow object
- VsCodeWindow object
ms.assetid: cf5fe926-e784-4098-bc01-cac49c7c55c6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8b1a3c19d349b84b10e0f36aca57a24aaac0d521
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56688764"
---
# <a name="vscodewindow-object"></a>VSCodeWindow nesnesi
Bir veya daha fazla metin görünümleri genellikle içerebilir bir özel belge penceresi bir kod penceredir <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView> nesne.

 Bu mimari, kod penceresi bir pencere çerçevesinde bir belge penceresi ' dir. İşlevsel olarak, kod penceresi ek özelliklere sahip bir belge penceresi yalnızca ' dir. Çok Belgeli Arabirim (MDI) modunda kod penceresinde MDI alt çerçeve ' dir. Daha fazla bilgi için [eski API'sini kullanarak kod windows özelleştirme](../extensibility/customizing-code-windows-by-using-the-legacy-api.md).

 Aşağıdaki tablo, arabirimlerini içerir <xref:Microsoft.VisualStudio.TextManager.Interop.VsCodeWindow> nesne.

|Yöntem|Açıklama|
|------------|-----------------|
|<xref:Microsoft.VisualStudio.OLE.Interop.IServiceProvider>|Bir genel benzersiz tanıtıcısı (GUID) tanımlayan bir hizmet bulmak için bir genel erişim mekanizması sağlar.|
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindow>|Bir veya daha fazla kod görünümleri içeren birden çok belge arabirimi (MDI) alt temsil eder.|
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane>|Pencere çerçevesi doldurur.|

## <a name="see-also"></a>Ayrıca bkz.
- <xref:Microsoft.VisualStudio.OLE.Interop.IServiceProvider>
- [Şekil Düzenle](https://www.microsoft.com/download/details.aspx?id=55984)