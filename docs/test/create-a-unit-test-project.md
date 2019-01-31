---
title: Birim testi projesi oluşturma
ms.date: 01/29/2019
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 813829e1e4024a38415cd9cef6da9fa7ca2ed87b
ms.sourcegitcommit: 9866740aec05d1a3a5dc3b4b6d2ceaeecbd3fc29
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55424414"
---
# <a name="create-a-unit-test-project"></a>Birim testi projesi oluşturma

Birim testleri, test altındaki kod yapısına genellikle yansıtır. Örneğin, her kod projesini ürün için birim testi projesi oluşturulması. Ayrı bir çözümde de olabilir veya üretim kodu aynı çözümde test projesini olabilir. Test projeleri bir çözümde birden çok birim olabilir.

> [!NOTE]
> Yerel kod için birim konumunu testleri ve test Proje yapısı bu makalede açıklanan yapısı farklı olabilir. Daha fazla bilgi için [C/C++ için birim testleri yazma](writing-unit-tests-for-c-cpp.md).

## <a name="to-create-a-unit-test-project"></a>Birim testi projesi oluşturmak için

1. Üzerinde **dosya** menüsünde seçin **yeni** seçip **proje**. Veya basın **Ctrl**+**Shift**+**N**.

2. İçinde **yeni proje** iletişim kutusunda **yüklü** düğümü, test projeniz için kullanın ve ardından istediğiniz dili seçin **Test**.

3. Microsoft birim testi çerçevelerini birini kullanmak üzere, **Birim Test projesi** proje şablonları listesinden. Aksi takdirde, kullanmak istediğiniz test çerçevesi biriminin proje şablonu seçin. Projeyi adlandırın ve ardından **Tamam**.

4. Birim test projenizde, test edilen kod bir başvuru ekleyin. Aynı çözümdeki bir kod projesine bir başvuru eklemek için:

   1. Test projesini seçin **Çözüm Gezgini**.

   2. Üzerinde **proje** menüsünde seçin **Başvuru Ekle**.

   3. İçinde **başvuru Yöneticisi**seçin **çözüm** düğümünde **projeleri**. Test edin ve ardından istediğiniz kod projesi seçin **Tamam**.

   Test etmek istediğiniz kod başka bir konumda olup olmadığını, [bir projedeki başvuruları yönetme](../ide/managing-references-in-a-project.md) başvuru ekleme hakkında daha fazla bilgi için.

## <a name="next-steps"></a>Sonraki adımlar

Aşağıdaki bölümlerden birine bakın:

**Birim testleri yazma**

- [Birim testi kod](../test/unit-test-your-code.md)

- [C/C++ için birim testleri yazma](writing-unit-tests-for-c-cpp.md)

- [MSTest framework birim testleri kullanın](using-microsoft-visualstudio-testtools-unittesting-members-in-unit-tests.md)

**Birim testlerini çalıştırma**

- [Test Gezgini ile birim testleri çalıştırma](../test/run-unit-tests-with-test-explorer.md)