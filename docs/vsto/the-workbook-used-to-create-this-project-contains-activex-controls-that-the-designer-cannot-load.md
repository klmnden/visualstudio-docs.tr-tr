---
title: Bu projeyi oluşturmak için kullanılan çalışma kitabı tasarımcının yükleyemeyeceği ActiveX denetimleri içeriyor
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VST.SelectDocWizard.ContainsActiveXControls
dev_langs:
- VB
- CSharp
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 27feb1c6a85740d8a9287ce3a2a47800595e178a
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71253787"
---
# <a name="the-workbook-used-to-create-this-project-contains-activex-controls-that-the-designer-cannot-load"></a>Bu projeyi oluşturmak için kullanılan çalışma kitabı tasarımcının yükleyemeyeceği ActiveX denetimleri içeriyor
  Program aracılığıyla bir Word belgesi veya Excel çalışma sayfasına bir denetim eklediğinizde, belgeyi veya çalışma kitabını kaydettiğinizde ve sonra belge veya çalışma kitabını temel alan yeni bir belge düzeyi çözümü oluşturduğunuzda bu hata görüntülenir.

 Denetimin yönetilen türünü açıklayan bilgiler belge veya çalışma kitabıyla birlikte kaydedilmez. Bu belgeye veya çalışma kitabına dayalı yeni bir çözüm oluşturduğunuzda, Visual Studio 'Nun denetimi konak öğesi tasarımcısında yüklemek için yeterli bilgi yok.

## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için

1. Belgeyi veya çalışma kitabını açın.

2. Çalışma zamanında eklenen denetimleri kaldırın. Bunu belge veya çalışma kitabında seçerek ve **Delete** tuşuna basarak yapabilirsiniz.

3. Belge veya çalışma kitabı temelinde belge düzeyi çözümü oluşturun.

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Visual Studio 'da Office projeleri oluşturma](../vsto/how-to-create-office-projects-in-visual-studio.md)
- [Çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
