---
title: 'Nasıl yapılır: Metin dosyalarını program aracılığıyla çalışma kitapları olarak açma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- workbooks, opening text files as
- text [Office development in Visual Studio], text files
- text files, opening as workbooks
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 61e51f6274bc22ed0d34d33f5ff85bfbfbd927bd
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62812468"
---
# <a name="how-to-programmatically-open-text-files-as-workbooks"></a>Nasıl yapılır: Metin dosyalarını program aracılığıyla çalışma kitapları olarak açma
  Bir çalışma kitabı olarak bir metin dosyasını açabilirsiniz. Açmak istediğiniz dosyanın adını geçmesi gerekir. Hangi satır numarası üzerinde ayrıştırma Başlat ve veri dosyasındaki sütun biçimi gibi çeşitli isteğe bağlı parametreleri belirtebilirsiniz.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="example"></a>Örnek
 [!code-csharp[Trin_VstcoreExcelAutomation#80](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#80)]
 [!code-vb[Trin_VstcoreExcelAutomation#80](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#80)]

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek aşağıdaki bileşenleri gerektirir:

- Adlı bir virgülle ayrılmış metin dosyası `Test.txt` en az üç satırlık metin içeren.

- Metin dosyası `Test.txt` c sürücüsüne depolanması

## <a name="see-also"></a>Ayrıca bkz.
- [Çalışma kitaplarıyla çalışma](../vsto/working-with-workbooks.md)
- [Nasıl yapılır: Program aracılığıyla çalışma kitaplarını açma](../vsto/how-to-programmatically-open-workbooks.md)
- [Nasıl yapılır: Yeni çalışma kitaplarını program aracılığıyla oluşturma](../vsto/how-to-programmatically-create-new-workbooks.md)
- [Nasıl yapılır: Çalışma kitaplarını program aracılığıyla kaydetme](../vsto/how-to-programmatically-save-workbooks.md)
- [Nasıl yapılır: Çalışma kitaplarını program aracılığıyla kapatma](../vsto/how-to-programmatically-close-workbooks.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
