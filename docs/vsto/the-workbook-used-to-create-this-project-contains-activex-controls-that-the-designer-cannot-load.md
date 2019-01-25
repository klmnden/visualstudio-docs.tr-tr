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
ms.openlocfilehash: d8c42a1d1a6745daca8d83d3f21916253e70fdae
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54867448"
---
# <a name="the-workbook-used-to-create-this-project-contains-activex-controls-that-the-designer-cannot-load"></a>Bu projeyi oluşturmak için kullanılan çalışma kitabı tasarımcının yükleyemeyeceği ActiveX denetimleri içeriyor
  Bu hata, bir Word belgesi için bir denetim eklediğinizde veya Excel çalışma programlı olarak belge veya çalışma kitabını kaydedin ve belge veya çalışma kitabını temel alan yeni bir belge düzeyi çözümü oluşturup görüntülenir.  
  
 Yönetilen denetim türünü açıklayan bilgileri, belge veya çalışma kitabı ile birlikte kaydedilmez. Bu belge veya çalışma kitabını temel alan yeni bir çözüm oluşturduğunuzda, Visual Studio ana bilgisayar öğesi Tasarımcısı'nda denetimi yüklemek için yeterli bilgi yok.  
  
## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
1.  Belge veya çalışma kitabını açın.  
  
2.  Çalışma zamanında eklenen denetimlerini kaldırma. Belge veya çalışma kitabı ve tuşlarına basarak seçerek bunu yapabilirsiniz **Sil** anahtarı.  
  
3.  Belge veya çalışma kitabını temel alan bir belge düzeyi çözümü oluşturun.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Visual Studio'da Office projeleri oluşturma](../vsto/how-to-create-office-projects-in-visual-studio.md)   
 [Office belgelerine çalışma zamanında denetimler ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)  
