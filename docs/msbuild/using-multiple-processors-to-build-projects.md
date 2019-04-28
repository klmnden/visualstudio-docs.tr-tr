---
title: Projeleri derlemek için birden çok işlemci kullanma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- multiple processors
- MSBuild, multiple processor systems
ms.assetid: 49fa36c9-8e14-44f5-8a2b-34146cf6807b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4af67aa3961b92b55abfdcf7a811daef284ca523
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62970841"
---
# <a name="use-multiple-processors-to-build-projects"></a>Projeleri derlemek için birden çok işlemci kullanma
MSBuild, birden çok işlemci veya birden çok çekirdekli işlemcilere sahip sistemler yararlanabilirsiniz. Bir yapı işlemi için kullanılabilir her işlemci oluşturulur. Sistem dört işlemci varsa, örneğin, ardından dört yapı işlemlerini oluşturulur. [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] Bu yapılar aynı anda işleyebilir ve bu nedenle genel derleme süresi azalır. Ancak, paralel yapı, yapı işlemlerini nasıl ortaya bazı değişiklikler ortaya çıkarır. Bu konu, bu değişiklikleri açıklamaktadır.

## <a name="project-to-project-references"></a>Projeden projeye başvurular
 Zaman [!INCLUDE[vstecmsbuildengine](../msbuild/includes/vstecmsbuildengine_md.md)] yalnızca bir kez başvuru yapıların karşılaşıyorsa, bir projeyi derlemek için paralel kullanırken bir projeden projeye (P2P) başvuru oluşturur. İki proje aynı P2P başvurusu varsa, başvuru her proje için yeniden değil. Bunun yerine, yapı altyapısının aynı bağımlı her iki proje P2P başvuru döndürür. Gelecekteki isteklerde oturum aynı hedef için aynı P2P başvuru sağlanır.

## <a name="cycle-detection"></a>Döngü algılama
 Döngü algılama İşlevler, aynı, önceden olduğu gibi [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] 2.0, tek farkı, artık [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] farklı bir saat veya yapı içinde döngüsü algılanması bildirebilirsiniz.

## <a name="errors-and-exceptions-during-parallel-builds"></a>Hatalar ve özel durumlar paralel yapılar sırasında
 Paralel yapılar hatalar ve özel durumlar farklı zamanlarda, paralel olmayan bir derlemede yapın ve bir proje değil oluşturduğunuzda bir proje yapılarında devam ortaya çıkabilir. [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] başarısız bir paralel derleme herhangi bir proje yapı durdurmaz. Diğer projeler bunların başarılı veya başarısız kadar oluşturmaya devam edin. Ancak, varsa <xref:Microsoft.Build.Framework.IBuildEngine.ContinueOnError%2A> hata oluşması durumunda hiçbir derleme durur etkinleştirildi.

## <a name="visual-c-project-vcproj-and-solution-sln-files"></a>Visual C++ projesi (.vcproj) ve çözüm (.sln) dosyaları
 Her ikisi de [!INCLUDE[vcprvc](../code-quality/includes/vcprvc_md.md)] projeleri (*.vcproj*) ve çözüm (*.sln*) dosyaları geçilebilir [MSBuild görevi](../msbuild/msbuild-task.md). İçin [!INCLUDE[vcprvc](../code-quality/includes/vcprvc_md.md)] projeleri VCWrapperProject çağrılır, ardından iç [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] Proje oluşturulur. İçin [!INCLUDE[vcprvc](../code-quality/includes/vcprvc_md.md)] çözümleri, bir SolutionWrapperProject oluşturulur ve ardından dahili [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] Proje oluşturulur. Her iki durumda da elde edilen proje değerlendirilir diğer aynı [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] proje.

## <a name="multi-process-execution"></a>Birden çok işlem yürütme
 Neredeyse tüm derlemeyle ilgili etkinlikler, geçerli dizin yolu ile ilgili hataları önlemek için derleme işlem süresince sabit kalması gerekir. Bu nedenle, farklı iş parçacıkları üzerinde projeleri çalıştırılamaz [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] çünkü birden çok dizin oluşturulmasına neden olur.

 Bu sorundan kaçınmak, ancak yine de çok işlemcili yapılar etkinleştirmek için [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] "işleminin kullandığı yalıtım." İşlem yalıtım kullanarak [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] en fazla oluşturabilirsiniz `n` işlemleri, burada `n` sistemde kullanılabilir işlemci sayısına eşittir. Örneğin, varsa [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] derlemeleri yapı süreçlerini, yapı yalnızca iki sonra iki işlemciye sahip bir sistemde bir çözüm oluşturulur. Bu işlemler Çözümdeki tüm projeleri derlemek için yeniden kullanılır.

## <a name="see-also"></a>Ayrıca bkz.
- [Paralel olarak birden çok proje derleme](../msbuild/building-multiple-projects-in-parallel-with-msbuild.md)
- [Görevler](../msbuild/msbuild-tasks.md)