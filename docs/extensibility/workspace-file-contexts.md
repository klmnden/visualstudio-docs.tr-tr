---
title: Visual Studio'da dosya bağlamları çalışma | Microsoft Docs
ms.date: 02/21/2018
ms.topic: conceptual
author: vukelich
ms.author: svukel
manager: viveis
ms.workload:
- vssdk
ms.openlocfilehash: 36f986db6f2c7b483b46060e1f514acc8dd9e758
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62952873"
---
# <a name="workspace-file-contexts"></a>Çalışma alanı dosyası bağlamları

Tüm Öngörüler [Klasör Aç](../ide/develop-code-in-visual-studio-without-projects-or-solutions.md) çalışma alanları "uygulayan dosya bağlam sağlayıcıları tarafından" üretilen <xref:Microsoft.VisualStudio.Workspace.IFileContextProvider> arabirimi. Bu uzantıları klasörleri değişikliklerde görünebilir veya MSBuild dosyalarını ve derleme görevleri dosyalarını, dosyaları, dosya bağlamını tanımlamak ihtiyaç duydukları ınsights accumulate için Paket bağımlılıklarını vb. algılayın. Tek başına bir dosya bağlamı, herhangi bir işlem gerçekleştirmez, ancak bunun yerine başka bir uzantı, üzerinde işlem yapabileceğiniz veri sağlar.

Her <xref:Microsoft.VisualStudio.Workspace.FileContext> sahip bir `Guid` veri türünü tanımlayan bu taşıyan ilişkili. Bu çalışma alanı kullanır `Guid` daha sonra aracılığıyla verileri kullanır uzantıları ile eşleştirme amacıyla <xref:Microsoft.VisualStudio.Workspace.FileContext.Context> özelliği. Bir dosya bağlam sağlayıcısına hangi dosya bağlamını tanımlayan meta verileriyle aktarılır `Guid`s, verileri oluşturabilir.

Tanımlandıktan sonra bir dosya bağlamı herhangi bir sayıda dosyaları veya Çalışma klasörleri ile ilişkilendirilebilir. Belirtilen dosya veya klasör, dosya bağlamları herhangi bir sayıda ile ilişkili olabilir. Çoktan çoğa bir ilişkidir.

Dosya bağlamları için en yaygın senaryoları, derleme, hata ayıklama ve dil Hizmetleri ilgilidir. Daha fazla bilgi için bu senaryolarla ilgili diğer konulara bakın.

## <a name="file-context-lifecycle"></a>Dosya içeriği yaşam döngüsü

Ömürleri bir `FileContext` belirleyici olduğu. Herhangi bir zamanda bir bileşen bazı içerik türleri kümesi için zaman uyumsuz olarak talep edebilir. Bazı alt istek içerik türleri desteği sağlayıcıları sorgulanır. `IWorkspace` Orta-man üzerinden sağlayıcıları ve tüketici arasında görür örneği <xref:Microsoft.VisualStudio.Workspace.IWorkspace.GetFileContextsAsync%2A> yöntemi. Tüketiciler istek bir bağlamı ve bağlama, diğer bir içerik isteği ve uzun süreli bir başvuru korumak göre kısa vadeli bazı eylemler gerçekleştirme.

Değişiklikleri eskir bir dosya bağlamı neden dosyalara gerçekleşebilir. Sağlayıcı üzerinde bir olay tetikleyebilir `FileContext` güncelleştirmeleri tüketicilerinin bildirir. Örneğin, bir derleme bağlamı için bazı dosyası sağlanır, ancak bu bağlamı bir disk değişikliği geçersiz kılar, daha sonra olay özgün üretici çağırabilirsiniz. Yine, başvuran herhangi bir tüketiciye `FileContext` sonra yeni bir sorgulayabilirsiniz `FileContext`.

>[!NOTE]
>Tüketiciler için herhangi bir gönderme modeli yoktur. Tüketiciler olmaz bildirim bir sağlayıcının yeni `FileContext` kendi istekten sonra.

## <a name="expensive-file-context-computations"></a>Pahalı dosya bağlam hesaplamaları

Özellikle bir sağlayıcı dosyaları arasındaki ilişki çözmek gerektiğinde diskten okuma dosya içeriklerini pahalı olabilir. Örneğin, bazı kaynak dosyanın dosya bağlamı için bir sağlayıcı sorgulanan, ancak proje dosyasından meta veri dosyası bağlam bağlıdır. MSBuild ile değerlendirme ya da proje dosyası ayrıştırma pahalıdır. Bunun yerine, uzantı verebilirsiniz bir `IFileScanner` oluşturmak için `FileDataValue` çalışma dizini oluşturma sırasında veri. Artık dosya bağlamları için sorulduğunda `IFileContextProvider` ilişkin dizinlenmiş verileri hızla sorgulayabilir. Dizin oluşturma ile ilgili daha fazla bilgi için bkz: [çalışma dizinini](workspace-indexing.md) konu.

>[!WARNING]
>Diğer yollarını dikkatli olun, `FileContext` hesaplamak pahalı olabilir. Bazı kullanıcı Arabirimi etkileşimleri zaman uyumlu ve yüksek hacimli üzerinde kullanan `FileContext` istekleri. Bir düzenleyici sekmesini açarak ve açma bir **Çözüm Gezgini** bağlam menüsü. Bu Eylemler, istekleri yazın, birçok derleme bağlamı olun.

## <a name="file-context-related-apis"></a>Dosya bağlamını ilgili API'ler

- <xref:Microsoft.VisualStudio.Workspace.FileContext> veri ve meta veriler tutar.
- <xref:Microsoft.VisualStudio.Workspace.IFileContextProvider> ve <xref:Microsoft.VisualStudio.Workspace.IFileContextProvider`1> dosya bağlamını oluşturun.
- <xref:Microsoft.VisualStudio.Workspace.ExportFileContextProviderAttribute> bir dosya bağlam sağlayıcısına dışarı aktarır.
- <xref:Microsoft.VisualStudio.Workspace.IWorkspace.GetFileContextsAsync%2A> Tüketiciler için dosya içerikleri almak için kullanılır.
- <xref:Microsoft.VisualStudio.Workspace.Build.BuildContextTypes> Klasör Aç tüketecektir derleme içerik türlerini tanımlar.

## <a name="file-context-actions"></a>Dosya içeriği eylemleri

Ancak bir `FileContext` kendisi hakkında bazı dosyalar yalnızca verileri olan bir <xref:Microsoft.VisualStudio.Workspace.IFileContextAction> express ve o veri üzerinde oynama yapmak için bir yoldur. `IFileContextAction` kendi kullanımı esnektir. İki, en yaygın örnekleri oluşturma, hata ayıklama ve gelir.

## <a name="reporting-progress"></a>İlerleme durumunu bildirme

<xref:Microsoft.VisualStudio.Workspace.IFileContextActionBase.ExecuteAsync%2A> Yöntemi geçirilir `IProgress<IFileContextActionProgressUpdate>`, ancak bağımsız değişken, tür olarak kullanılmamalıdır. `IFileContextActionProgressUpdate` boş bir arabirim ve çağırma `IProgress<IFileContextActionProgressUpdate>.Report(IFileContextActionProgressUpdate)` fırlatabilir `NotImplementedException`. Bunun yerine, `IFileContextAction` bağımsız değişken olarak senaryo için gerekli başka bir türe dönüştürmeniz gerekir.

Visual Studio tarafından sağlanan türleri hakkında daha fazla bilgi için ilgili senaryonun belgelerine bakın.

## <a name="file-context-action-related-apis"></a>Dosya bağlamı eylemi ilgili API'ler

- <xref:Microsoft.VisualStudio.Workspace.IFileContextAction> dayalı bazı davranış yürüten bir `FileContext`.
- <xref:Microsoft.VisualStudio.Workspace.IFileContextActionProvider> örneklerini oluşturur `IFileContextAction`.
- <xref:Microsoft.VisualStudio.Workspace.ExportFileContextActionProviderAttribute> türü verir `IWorkspaceProviderFactory<IFileContextActionProvider>`.

## <a name="file-watching"></a>Dosya izleme

Bir çalışma alanı dosyası için değişiklik bildirimleri dinler ve sağlar <xref:Microsoft.VisualStudio.Workspace.IFileWatcherService> aracılığıyla <xref:Microsoft.VisualStudio.Workspace.WorkspaceServiceHelper.GetFileWatcherService%2A>. Dosya bildirim olayları "ExcludedItems" ayarıyla eşleşen dosyaları oluşturmaz. Olaylar arasındaki bir eşik bildirimi basitleştirme ve yinelenen azaltma için kullanılır. Bir dosya değişikliği için react gerektiğinde, bu hizmete abone olmalıdır.

>[!TIP]
>Bir çalışma alanının [dizin oluşturma hizmeti](workspace-indexing.md) varsayılan olarak dosya olayları kaydeder. Dosya ekleme ve değişiklik neden olacak ilgili `IFileScanner`söz konusu dosya için yeni veriler için çağrılacak s olayları. Dizinlenmiş verileri dosyaların silinmesi kaldıracak. Abone olmanız gerekmez, `IFileScanner` için dosya İzleyicisi hizmeti.

## <a name="next-steps"></a>Sonraki adımlar

* [Dizin oluşturma](workspace-indexing.md) -çalışma dizinini toplar ve çalışma alanı hakkında bilgileri kalıcıdır.
* [Çalışma alanları](workspaces.md) -çalışma kavramları ve ayarlarını depolama inceleyin.
