---
title: Office projelerinde .NET Framework hedefleme için değişiklikler tasarlama
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office development in Visual Studio 2010, what's new
- what's new [Office development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 74cb79a68298bb1c544b0f0646787e82e04cb810
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255168"
---
# <a name="changes-to-the-design-of-office-projects-that-target-the-net-framework-4-or-the-net-framework-45"></a>.NET Framework 4 ' ü veya .NET Framework 4,5 ' i hedefleyen Office projelerinin tasarımında yapılan değişiklikler
  ' Den itibaren, Visual Studio, [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya sonraki sürümlerini hedefleyen Office projelerinin tasarımında bazı değişiklikler getirmiştir. [!INCLUDE[vs_dev10_long](../sharepoint/includes/vs-dev10-long-md.md)] Visual Studio 'nun önceki sürümlerindeki Office projelerine alışkın değilseniz, .NET Framework 4,0 veya üzeri sürümlerini hedefleyen Office projeleri geliştirebilmeniz için bu değişikliklerden haberdar olmanız gerekir. Varsayılan olarak, Visual Studio 2013 veya üzeri kullanarak oluşturduğunuz tüm projeler .NET Framework 4,0 veya üstünü hedefleyin.

 Aşağıdaki bölümlerde bu Office proje tasarım değişiklikleri açıklanır.

## <a name="understand-the-interface-based-design-of-the-visual-studio-2010-tools-for-office-runtime"></a>Office çalışma zamanı için Visual Studio 2010 araçları 'nın arabirim tabanlı tasarımını anlama
 [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] Veya sonraki bir sürümü hedefleyen bir Office projesi geliştirirken, Office çalışma zamanı için Visual Studio 2010 araçlarında kullandığınız türlerin çoğu arayüzlerdir. Bu, ' nin, [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]bu türlerin sınıflar olduğu önceki sürümlerinden büyük bir değişimdir. Örneğin, [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya sonraki bir sürümünü hedeflediğinizde <xref:Microsoft.Office.Tools.Excel.Worksheet> , ve <xref:Microsoft.Office.Tools.Word.Document> türleri sınıflar yerine arayüzlerdir. Daha fazla bilgi için bkz. [Office çalışma zamanına genel bakış Visual Studio Araçları](../vsto/visual-studio-tools-for-office-runtime-overview.md).

 Daha önceki sürümlerinde [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]doğrudan örneklenebilen herhangi bir tür için artık bu türlerin örneklerini almak üzere `Globals.Factory` nesne yöntemlerini kullanacaksınız. Örneğin, <xref:Microsoft.Office.Tools.Excel.SmartTag> arabirimini uygulayan bir nesne almak için `Globals.Factory.CreateSmartTag` yöntemini kullanın. Daha fazla bilgi için aşağıdaki konulara bakın:

- [.NET Framework 4 ' e veya .NET Framework 4,5 ' ye geçirebileceğiniz Excel ve Word projelerini güncelleştirme](../vsto/updating-excel-and-word-projects-that-you-migrate-to-the-dotnet-framework-4-or-the-dotnet-framework-4-5.md)

- [.NET Framework 4 ' e veya .NET Framework 4,5 ' ye geçirebileceğiniz Office Projelerindeki Şerit özelleştirmelerini güncelleştirme](/visualstudio/vsto/update-ribbon-customizations-in-office-projects-to-migrate-to-dotnet-framework-4-or-4-5)

- [.NET Framework 4 ' e veya .NET Framework 4,5 ' ye geçirebileceğiniz Outlook Projelerindeki Form bölgelerini güncelleştirme](../vsto/updating-form-regions-in-outlook-projects-that-you-migrate-to-the-dotnet-framework-4-or-the-dotnet-framework-4-5.md)

### <a name="new-base-classes-in-office-projects"></a>Office projelerinde yeni temel sınıflar
 Office çalışma zamanı için Visual Studio 2010 araçları 'nın yeni arabirim tabanlı tasarımı,, ve `ThisDocument` `ThisAddIn`gibi Office projelerinde `ThisWorkbook`oluşturulan sınıfları etkiler. .NET Framework 3,5 ' i ve Framework 'ün önceki sürümlerini hedefleyen Office projelerinde, oluşturulan bu sınıflar [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] , ve `Microsoft.Office.Tools.AddIn`gibi sınıflarından `Microsoft.Office.Tools.Word.Document` `Microsoft.Office.Tools.Excel.Worksheet`türetilir. [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] Veya daha sonra hedeflenen projelerde, bu [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] sınıflar artık arayüzlerdir. Bu nedenle, Office projelerindeki oluşturulan sınıflar bundan böyle kendi uygulamasını bundan türemez. Bunun yerine, oluşturulan sınıflar, ve <xref:Microsoft.Office.Tools.Word.DocumentBase> <xref:Microsoft.Office.Tools.AddInBase>gibi yeni temel sınıflardan <xref:Microsoft.Office.Tools.Excel.WorksheetBase>türetilir. Daha fazla bilgi için bkz. [Program VSTO eklentileri](../vsto/programming-vsto-add-ins.md) ve [Program belge düzeyi özelleştirmeleri](../vsto/programming-document-level-customizations.md).

 Temel sınıflar [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] yeniden dağıtılabilir bir parçası değildir. Bunun yerine, Visual Studio 'da bulunan yardımcı programlar Derlemeleriyle tanımlanmıştır. Bu derlemeler Office projeleri oluşturduğunuzda çıkış klasörüne kopyalanır ve çözümünüz ile birlikte dağıtılması gerekir. Yardımcı programlar derlemeleri hakkında daha fazla bilgi için, bkz. [Office çalışma zamanı için Visual Studio Araçları derlemeler](../vsto/assemblies-in-the-visual-studio-tools-for-office-runtime.md).

## <a name="breaking-changes-in-office-projects-that-are-retargeted-to-the-net-framework-4"></a>.NET Framework 4 ' e yeniden hedeflenmiş Office projelerindeki son değişiklikler
 Aşağıdaki tabloda, [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya daha sonra yeniden hedeflenen Office projelerinde karşılaşabileceğiniz ana son değişiklikler listelenmiştir. Daha fazla ayrıntı için bkz. [Office çözümlerini .NET Framework 4 veya sonraki bir sürüme geçirme](../vsto/migrating-office-solutions-to-the-dotnet-framework-4-or-later.md).

|Son değişiklik|Sonucudur|
|---------------------|-----------------|
|<xref:System.Security.SecurityTransparentAttribute> Office projelerinde artık kullanılmıyor veya desteklenmiyordur.|Bu özniteliği, Visual Studio 2008 ' den yükselttiğiniz Office projelerindeki AssemblyInfo kod dosyasından kaldırmanız gerekir. Daha fazla bilgi için, [.NET Framework 4 ' e veya .NET Framework 4,5 ' a geçirebileceğiniz Office projelerini çalıştırmak Için gereken değişiklikler](../vsto/required-changes-to-run-office-projects-that-you-migrate-to-the-dotnet-framework-4-or-the-dotnet-framework-4-5.md)konusuna bakın.|
|**ExcelLocale1033Attribute** artık Excel projelerinde kullanılmamaktadır veya desteklenmez.|Bu özniteliği Excel projelerindeki *AssemblyInfo* kod dosyasından kaldırmanız gerekir. Daha fazla bilgi için, [.NET Framework 4 ' e veya .NET Framework 4,5 ' a geçiş yaptığınız Excel ve Word projelerini güncelleştirme](../vsto/updating-excel-and-word-projects-that-you-migrate-to-the-dotnet-framework-4-or-the-dotnet-framework-4-5.md)bölümüne bakın.|
|**Şerit (görsel Tasarımcı)** proje öğelerinin programlama modeli değişti.|Projenizdeki herhangi bir şerit öğesi için arka plan kod dosyasını değiştirmeniz gerekir. Ayrıca, çalışma zamanında Şerit denetimlerini örnekleyen, Şerit olaylarını işleyen veya Şerit bileşeninin konumunu programlı bir şekilde ayarlayan herhangi bir kodu değiştirmeniz gerekir. Daha fazla bilgi için bkz. [.NET Framework 4 ' e veya .NET Framework 4,5 ' ye geçirebileceğiniz Office Projelerindeki Şerit özelleştirmelerini güncelleştirme](/visualstudio/vsto/update-ribbon-customizations-in-office-projects-to-migrate-to-dotnet-framework-4-or-4-5).|
|Outlook form bölgelerinin programlama modeli değişti.|Projenizdeki herhangi bir form bölgesi için arka plan kod dosyasını ve belirli form bölgesi sınıflarını çalışma zamanında örnekleyen tüm kodları değiştirmeniz gerekir. Daha fazla bilgi için, bkz. [.NET Framework 4 ' e veya .NET Framework 4,5 'e geçirdiğinizde Outlook Projelerindeki güncelleştirme form bölgeleri](../vsto/updating-form-regions-in-outlook-projects-that-you-migrate-to-the-dotnet-framework-4-or-the-dotnet-framework-4-5.md).|
|Excel ve Word projelerindeki akıllı etiketler için programlama modeli değişmiştir. Akıllı Etiketler ve [!INCLUDE[Word_14_short](../vsto/includes/word-14-short-md.md)]' de [!INCLUDE[Excel_14_short](../vsto/includes/excel-14-short-md.md)] kullanım dışıdır.|Çözümünüz Akıllı Etiketler kullanıyorsa, projeyi oluşturduğunuzda hatalar oluşur. Ve [!INCLUDE[Excel_14_short](../vsto/includes/excel-14-short-md.md)] [!INCLUDE[vs_dev12](../vsto/includes/vs-dev12-md.md)] içinde Akıllı Etiketler kullanım dışı olduğundan, veya sonraki kısımlarında çözümü test etmeden ve hata ayıklamadan önce etiketleri kaldırmanız gerekir. [!INCLUDE[Word_14_short](../vsto/includes/word-14-short-md.md)]|
|`GetVstoObject` Ve`HasVstoObject` yöntemlerinin sözdizimi değiştirildi|Bu yöntemlere, birincil `Globals.Factory` birlikte çalışma derlemelerinden (PIA 'lar) yerel nesneler üzerinde eriştiğinizde veya projenizdeki `Globals.Factory` özelliği tarafından döndürülen nesnede bu yöntemlere erişmeniz gerekir. Daha fazla bilgi için, [.NET Framework 4 ' e veya .NET Framework 4,5 ' a geçiş yaptığınız Excel ve Word projelerini güncelleştirme](../vsto/updating-excel-and-word-projects-that-you-migrate-to-the-dotnet-framework-4-or-the-dotnet-framework-4-5.md)bölümüne bakın.|
|Word içerik denetimlerinin olayları yeni temsilcilerle ilişkilendirilir.|Yeni temsilcileri belirtmek için Word içerik denetimlerinin olaylarını işleyen herhangi bir kodu değiştirmeniz gerekir. Daha fazla bilgi için, [.NET Framework 4 ' e veya .NET Framework 4,5 ' a geçiş yaptığınız Excel ve Word projelerini güncelleştirme](../vsto/updating-excel-and-word-projects-that-you-migrate-to-the-dotnet-framework-4-or-the-dotnet-framework-4-5.md)bölümüne bakın.|
|`OLEObject` Ve`OLEControl` sınıfları yeniden adlandırıldı.|Bunun yerine veya <xref:Microsoft.Office.Tools.Excel.ControlSite> <xref:Microsoft.Office.Tools.Word.ControlSite> nesnelerini kullanmak için bu sınıfların örneklerini kullanan herhangi bir kodu değiştirmeniz gerekir. Daha fazla bilgi için, [.NET Framework 4 ' e veya .NET Framework 4,5 ' a geçiş yaptığınız Excel ve Word projelerini güncelleştirme](../vsto/updating-excel-and-word-projects-that-you-migrate-to-the-dotnet-framework-4-or-the-dotnet-framework-4-5.md)bölümüne bakın.|
|`ThisWorkbook`, *N,, ve* gibi`ThisAddIn`konak öğesi sınıfları artık geçersiz kılabileceğiniz bir `Dispose` yöntem sağlamaz. `ThisDocument` `Sheet`|`Dispose` Yöntemi geçersiz kılmada `Shutdown` bulunan herhangi bir kodu konak öğesi `ThisAddIn_Shutdown`sınıfındaki olay işleyicisine taşımanız gerekir, örneğin,, ve sonra da konak öğesi sınıfınızdan `Dispose` yöntem geçersiz kılmayı kaldırın.|

## <a name="see-also"></a>Ayrıca bkz.
- [Office çözümlerini .NET Framework 4 veya sonraki sürümlere geçirme](../vsto/migrating-office-solutions-to-the-dotnet-framework-4-or-later.md)
- [Office geliştirme yenilikleri](https://msdn.microsoft.com/library/bf054af2-c896-4723-aa15-6381145b14bb)
- [Office çalışma zamanına genel bakış için Visual Studio Araçları](../vsto/visual-studio-tools-for-office-runtime-overview.md)
