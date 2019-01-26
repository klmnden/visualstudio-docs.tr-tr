---
title: MSTest onay sınıfları ve yöntemleri
ms.date: 06/07/2018
ms.prod: visual-studio-dev15
ms.topic: reference
helpviewer_keywords:
- Assert classes
- Assert methods
- unit tests, Assert classes
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 617f5f82f2d6ff2388325f8b623c87e0210ab340
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/26/2019
ms.locfileid: "55070662"
---
# <a name="use-assert-classes-for-unit-testing"></a>Birim testi için onay sınıflarını kullanma

Onay sınıfları kullanma <xref:Microsoft.VisualStudio.TestTools.UnitTesting> belirli işlevselliğini doğrulamak için ad alanı. Kod, uygulamanızın kodunda bir yöntemin bir birim sınaması metodunda uygular, ancak yalnızca Assert deyimleri eklerseniz kodun davranışı doğruluğunu rapor.

## <a name="kinds-of-asserts"></a>Tür, onaylar

<xref:Microsoft.VisualStudio.TestTools.UnitTesting> Onay sınıfları çeşitli ad alanı sağlar.

Test yönteminizde herhangi bir yöntem çağırabilirsiniz <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert?displayProperty=fullName> gibi sınıf <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert.AreEqual%2A?displayProperty=nameWithType>. <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert> Sınıfı aralarından seçim yapabileceğiniz birçok yöntem vardır ve birçok yöntem bazı aşırı yüklemeleri vardır.

### <a name="compare-strings-and-collections"></a>Karşılaştırma dizeleri ve koleksiyonları

Kullanım <xref:Microsoft.VisualStudio.TestTools.UnitTesting.CollectionAssert> nesne koleksiyonları karşılaştırma ya da bir koleksiyon durumunu doğrulamak için bir sınıf.

Kullanım <xref:Microsoft.VisualStudio.TestTools.UnitTesting.StringAssert> karşılaştırın ve dizeleri incelemek için sınıf. Bu sınıf gibi çeşitli kullanışlı yöntemler içeren <xref:Microsoft.VisualStudio.TestTools.UnitTesting.StringAssert.Contains%2A?displayProperty=nameWithType>, <xref:Microsoft.VisualStudio.TestTools.UnitTesting.StringAssert.Matches%2A?displayProperty=nameWithType>, ve <xref:Microsoft.VisualStudio.TestTools.UnitTesting.StringAssert.StartsWith%2A?displayProperty=nameWithType>.

### <a name="exceptions"></a>Özel Durumlar

<xref:Microsoft.VisualStudio.TestTools.UnitTesting.AssertFailedException> Bir test başarısız olduğunda özel durum harekete geçirilir. Bu zaman aşımına, beklenmeyen bir özel durum oluşturur veya üreten bir onay deyimi içeriyorsa, bir test başarısız bir **başarısız** sonucu.

<xref:Microsoft.VisualStudio.TestTools.UnitTesting.AssertInconclusiveException> Bir test sonucu üretir. her durum **yetersiz**. Genellikle, eklediğiniz bir <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert.Inconclusive%2A?displayProperty=nameWithType> hala açık değilse henüz çalıştırılmaya hazır belirtmek için çalıştığınız bir test bildirimi.

> [!NOTE]
> Bir testi çalıştırmak hazır değil olarak işaretlemek için alternatif bir strateji olduğunu <xref:Microsoft.VisualStudio.TestTools.UnitTesting.IgnoreAttribute> özniteliği. Ancak gelecekteki bir kolayca uygulanmadı testlerin sayısı bir rapor üretilemiyor dezavantajı vardır.

Yeni bir özel durum sınıfı assert yazdığınız taban sınıftan devralın <xref:Microsoft.VisualStudio.TestTools.UnitTesting.UnitTestAssertException> özel durum bir onaylama işlemi hatası yerine test veya üretim kodundan beklenmeyen bir özel durum olarak tanımlamak daha kolay.

Bir test yöntemi ile donatmak <xref:Microsoft.VisualStudio.TestTools.UnitTesting.ExpectedExceptionAttribute> özniteliği beklediğiniz bir yöntem uygulama kodunuzda tarafından oluşturulması için bir özel durum gerçekten durum doğrulamak için test yönteminin istediğinizde.

## <a name="see-also"></a>Ayrıca bkz.

- [Birim testi kod](../test/unit-test-your-code.md)