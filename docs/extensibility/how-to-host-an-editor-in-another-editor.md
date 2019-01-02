---
title: 'Nasıl Yapılır: Başka bir düzenleyicide bir düzenleyicide konak | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - host a nested editor
ms.assetid: 2b0eb705-fe94-4ca8-93e0-9dbd8ce61a44
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 6a9de111a1747e9f5451bff2c8bd3e5edf171d9a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53833613"
---
# <a name="how-to-host-an-editor-in-another-editor"></a>Nasıl Yapılır: Konak bir düzenleyicide başka bir düzenleyici

Visual Studio'da barındırma penceresi bir üst pencere olarak belirterek, içinde başka bir düzenleyicide barındırabilirsiniz. Bunu yapmak için parametreleri ayarlayın <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID2.VSFPROPID_ParentHwnd> ve <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID2.VSFPROPID_ParentFrame> alt pencere çerçevesi.

## <a name="to-set-up-the-window-frame-to-host-an-editor"></a>Bir düzenleyici barındırmak için Pencere çerçevesi ayarlamak için

1.  Bir düzenleyici bir alt pencere bölmesi oluşturarak barındırılan bir düzenleyici olarak belirleyin.

     Bu bölme, düzenleyicinin metni gidecekleri ' dir.

2.  Kullanarak barındırma Düzenleyicisi <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.OpenStandardEditor%2A> veya <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.OpenSpecificEditor%2A> yöntemi.

3.  Ayarlama <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID2.VSFPROPID_ParentHwnd> ve <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID2.VSFPROPID_ParentFrame> bu özellikler için parametre olarak geçirerek barındırılan Düzenleyicisi penceresi çerçeve uygulama özelliklerinde <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.SetProperty%2A> yöntemi, sırasıyla.

     Bu parametreleri almanız gerekiyorsa, bu özelliklerin geçirmek <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.GetProperty%2A> yöntemi.

4.  Çağrı <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.Show%2A> kapsanan Düzenleyicisi için yöntemi.

     Düzenleyici içeren Düzenleyicisi barındırılan bölmesinde görünür.

## <a name="robust-programming"></a>Güçlü programlama

**Uygulama Tasarımcısı** mimarları için Visual Studio Team Edition, başka bir düzenleyicide barındıran bir düzenleyici pencere çerçevesi örneğidir. **Uygulama Tasarımcısı** diğer tasarımcılar, sağ bölmede barındırır. Tasarımcı bölmesi (veya **özellikleri** sayfası) her biri bağımsız tasarımcıları içeren pencere çerçevesi için eklenir.