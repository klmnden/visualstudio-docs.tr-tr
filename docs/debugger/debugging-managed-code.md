---
title: Yönetilen kodda hata ayıklama | Microsoft Docs
ms.date: 09/23/2019
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging managed code
- debugging ASP.NET Web applications, managed code
- managed code, debugging
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: c94de629026cfa1b78429aaf2209b81eead7da4f
ms.sourcegitcommit: ea182703e922c74725045afc251bcebac305068a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71211205"
---
# <a name="debug-managed-code-c-visual-basic-f-ccli"></a>Yönetilen kodda hata ayıklamaC#(, Visual Basic F#, C++,/CLI)

Bu bölümde, yönetilen uygulamalar veya Visual Basic, C#ve C++/cligibi ortak dil çalışma zamanını hedefleyen dillerde yazılmış uygulamalar için yaygın hata ayıklama sorunları ve teknikleri ele alınmaktadır. Burada açıklanan teknikler, üst düzey tekniklerdir. [İlk olarak hata ayıklayıcıya bakın](../debugger/debugger-feature-tour.md).

## <a name="in-this-section"></a>Bu Bölümde

[Çıkış Penceresi tanılama Iletileri](../debugger/diagnostic-messages-in-the-output-window.md)\
Ve sınıflarını, çalışma zamanı iletilerini çıkış penceresine yazabileceğiniz şekilde açıklar. <xref:System.Diagnostics.Debug> <xref:System.Diagnostics.Trace> Bu sınıflar, belirtilen bir koşul başarısız olursa yürütmeyi kesintiye uğratmadan, yürütme ve bilgi çıkışının kesintiye girmeden bilgi çıktısını etkinleştiren çıkış yöntemlerini içerir.

[Yönetilen koddaki Onaylamalar](../debugger/assertions-in-managed-code.md)\
Yöntemler için `Assert` bağımsız değişken olarak belirttiğiniz test koşullarını Yönetilen koddaki onayları açıklar. Buna ek olarak, bu konuda örnek kod, <xref:System.Diagnostics.Debug> ve <xref:System.Diagnostics.Trace> sınıf yöntemleri hakkında bilgi, kod hata ayıklama ve yayın sürümlerindeki konular, yan etkiler, onaylama bağımsız değişkenleri, onaylama davranışını özelleştirme ve yapılandırma dosyaları sağlanmaktadır.

[Visual Basic deyimlerini durdur](../debugger/stop-statements-in-visual-basic.md)\
Kesme noktası ayarlamaya alternatif sağlayan ifadesiniaçıklar.`Stop` Örnek kod `Stop` Ayrıca, `Stop` ve deyimleri arasındaki karşılaştırmaların `End` yanı sıra, ve `Assert` deyimleriyle birlikte da sağlanır.

[İzlenecek yol: Windows formunda hata ayıklama](../debugger/walkthrough-debugging-a-windows-form.md)\
Windows formu oluşturmak ve bu formun hatalarını ayıklamak için adım adım yönergeler sağlar. Yönetilen bir Windows uygulamasının standart bir bileşeni olan Windows formu, en yaygın yönetilen uygulamalardan biridir. Bu izlenecek yol, C# Visual ve Visual Basic kullanır, ancak ile C++ Windows formu oluşturma teknikleri genellikle benzerdir.

[OnStart yönteminde hata ayıklama](../debugger/how-to-debug-the-onstart-method.md)\
Yönetilen bir Windows hizmeti `OnStart` yönteminde hata ayıklamanıza olanak tanımak için kod örnekleri sağlar. Bir Windows hizmeti `OnStart` yönteminde hata ayıklamak için, hizmetin benzetimini yapmak üzere birkaç satır kod eklemeniz gerekir.

[Karışık modda hata ayıklama](../debugger/debugging-mixed-mode-applications.md)\
Karışık modda uygulamalarda hata ayıklamayı açıklar. Bu, yerel kodu yönetilen kodla birleştiren tüm uygulamalar anlamına gelir.

[Hata: Sistemde bir çekirdek hata ayıklayıcısı etkinleştirildiğinden hata ayıklama mümkün değil](../debugger/error-debugging-isn-t-possible-because-a-kernel-debugger-is-enabled-on-the-system.md)\
Hata ayıklama modunda [!INCLUDE[win7](../debugger/includes/win7_md.md)]başlatılmış bir [!INCLUDE[winxp](../code-quality/includes/winxp_md.md)], [!INCLUDE[wiprlhext](../debugger/includes/wiprlhext_md.md)] [!INCLUDE[Win2kFamily](../code-quality/includes/win2kfamily_md.md)],, veya Windows NT sisteminde yönetilen kodda hata ayıklamaya çalıştığınızda oluşan bir hata iletisi açıklanır.

[JıT Iyileştirme ve hata ayıklama](../debugger/jit-optimization-and-debugging.md)\
Hata ayıklama sırasında JıT iyileştirmesinin etkilerini açıklar.

[LINQ ve DLıNQ hatalarını ayıklama](../debugger/debugging-linq.md)\
LINQ sorgularının hatalarını ayıklama tekniklerini açıklar.

[İzlenecek yol: Paralel uygulamada hata ayıklama](../debugger/walkthrough-debugging-a-parallel-application.md)\
Paralel bir uygulamada hata ayıklamak için **paralel görevler** ve **Paralel Yığınlar** araç pencerelerinin nasıl kullanılacağını açıklar.

## <a name="related-sections"></a>İlgili Bölümler

[IntelliTrace](../debugger/intellitrace.md)\
Uygulamanızın yürütme geçmişini IntelliTrace ile kaydederek daha hızlı ve kolay bir şekilde hata bulun. Kaydedilen olayları ve geri doğru ilerlemeden, uygulamanın durumunu zaman içinde önemli noktalarda incelemek için çağrılar yapın. Çok sayıda kesme noktası ayarlamadan veya uygulamanızı sık yeniden başlatarak kodunuzda hata ayıklayın. Visual Studio Enterprise gerektirir.

[Uygulamaları izleme ve Işaretleme](/dotnet/framework/debug-trace-profile/tracing-and-instrumenting-applications)\
Uygulamasının, çalışırken uygulamanın yürütülmesini izlemenin ve izleme deyimlerinin kodunuzda stratejik konumlarda yerleştirilmesi için gereken bir yol olan izlemeyi açıklar. Bu konu ayrıca, izleme ve izleme, izleme anahtarları, izleme dinleyicileri, bir uygulamadaki kod izleme, uygulama koduna izleme deyimleri ekleme ve ile koşullu olarak <xref:System.Diagnostics.Debug> <xref:System.Diagnostics.Trace> derleme için bir giriş bağlantıları sağlar. .

[/ASSEMBLYDEBUG](/cpp/build/reference/assemblydebug-add-debuggableattribute)\
İle <xref:System.Diagnostics.DebuggableAttribute> C++yazılmış koda eklenen bağlayıcı seçeneğini açıklar. Bu öznitelik, ile C++iliştirme gibi hata ayıklama özelliklerini kullanmak için gereklidir.

[Windows hizmet uygulamalarında hata ayıklama](/dotnet/framework/windows-services/how-to-debug-windows-service-applications)\
Windows hizmet uygulamalarında hata ayıklama, işleme ekleme, hizmetin `OnStart` yöntemindeki kodda hata ayıklama, ana yöntemdeki kod, kesme noktaları ayarlama ve hizmetler denetimini kullanma dahil olmak üzere önemli noktalar sağlar Hizmetinizi başlatmak, durdurmak, duraklatmak ve devam ettirmek için yönetici.

[Hata ayıklama ve profil oluşturma](/dotnet/framework/debug-trace-profile/index)\
.NET Framework uygulamalarda hata ayıklamayı ve yapılandırma gereksinimlerini açıklar.

[Betikte ve Web uygulamalarında hata ayıklama](/visualstudio/debugger/how-to-enable-debugging-for-aspnet-applications)\
Betiklerin ve Web uygulamalarında hata ayıklarken karşılaşabileceğiniz yaygın hata ayıklama sorunlarını ve tekniklerini açıklar.

## <a name="see-also"></a>Ayrıca bkz.

- [İzlenecek yol: Tasarım zamanında özel Windows Forms Denetimlerinde hata ayıkla](/dotnet/framework/winforms/controls/walkthrough-debugging-custom-windows-forms-controls-at-design-time)
- [Hata Ayıklayıcısı Güvenliği](../debugger/debugger-security.md)
- [Visual Studio’da hata ayıklama](../debugger/index.yml)
- [Hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md)