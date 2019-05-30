---
title: Gecikmeli belge yüklemesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: fb07b8e2-a4e3-4cb0-b04f-8eb11c491f35
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 42c8e7acb934c66baf804639e35deba59a9a8c81
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66312142"
---
# <a name="delayed-document-loading"></a>Gecikmeli belge yüklemesi

Bir kullanıcı bir Visual Studio çözümü yeniden açana, ilişkili belgelerin çoğu hemen yüklü değil. Belge pencere çerçevesi başlatma bekleyen durumda oluşturulur ve çalıştırılan Belge tablosu (RDT) (bir saplama çerçeve olarak adlandırılır) bir yer tutucu belge yerleştirilir.

Uzantınız, Visual Studio için genel bellek Ayak izi artırabilirsiniz bunlar yüklenmeden önce öğeleri belgelerde sorgulayarak gereksiz yere yüklenmesi proje belgelerini neden olabilir.

## <a name="document-loading"></a>Belge yükleme

Saplama çerçeve ve belge pencere çerçevesi sekmesini seçerek örneğin kullanıcı, belge eriştiğinde, tam olarak başlatılır. Belge Ayrıca, belgenin verilerini, doğrudan belge verileri almak için RDT erişme veya aşağıdaki çağrıları yaparak RDT dolaylı olarak erişmek isteyen bir uzantı tarafından başlatılabilir:

- Pencere çerçevesi <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.Show%2A> yöntemi.

- Pencere çerçevesi <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.GetProperty%2A> aşağıdaki özelliklerden birini yöntemi:

   - [__VSFPROPID.VSFPROPID_DocView](<xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID.VSFPROPID_DocView>)

   - [__VSFPROPID. VSFPROPID_ViewHelper](<xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID.VSFPROPID_ViewHelper>)

   - [__VSFPROPID.VSFPROPID_DocData](<xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID.VSFPROPID_DocData>)

   - [__VSFPROPID.VSFPROPID_AltDocData](<xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID.VSFPROPID_AltDocData>)

   - [__VSFPROPID. VSFPROPID_RDTDocData](<xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID.VSFPROPID_RDTDocData>)

   - [__VSFPROPID.VSFPROPID_SPProjContext](<xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID.VSFPROPID_SPProjContext>)

- Uzantınızı yönetilen kod kullanıyorsa değil, çağırmalıdır <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocumentTable.GetDocumentInfo%2A> emin olmadığınız sürece belgeyi başlatma bekleyen durumda değil veya tam olarak başlatılması için belgeyi istediğiniz. Yöntem her zaman belge döndürüldüğünden nedeni gerekiyorsa, oluşturma, veri nesnesi. Üzerinde yöntemlerden birini bunun yerine, çağırmalıdır `IVsRunningDocumentTable4` arabirimi.

- Uzantınızı C++ kullanıyorsa, geçirebilirsiniz `null` istemediğiniz parametreleri.

- Diğer özellikler için sormadan önce ilgili özelliklerini sormadan önce aşağıdaki yöntemlerden birini çağırarak yüklenirken gereksiz belge önleyebilirsiniz:

   - <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.GetProperty%2A> kullanarak [__VSFPROPID6. VSFPROPID_PendingInitialization](<xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID6.VSFPROPID_PendingInitialization>).

   - <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocumentTable4.GetDocumentFlags%2A>. Bu yöntem döndürür bir <xref:Microsoft.VisualStudio.Shell.Interop._VSRDTFLAGS4> için bir değer içeren bir nesne [_VSRDTFLAGS4. RDT_PendingInitialization](<xref:Microsoft.VisualStudio.Shell.Interop._VSRDTFLAGS4.RDT_PendingInitialization>) , belgenin henüz başlatılmadı.

Bir belge tam olarak başlatıldığında başlatan RDT olaya abone olarak bir belge yüklendiğinde bilgi edinebilirsiniz. İki olasılık vardır:

- Olay havuzu uyguluyorsa <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocTableEvents2>, abone olabileceğiniz <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocTableEvents2.OnAfterAttributeChangeEx%2A>,

- Aksi takdirde, abone olabileceğiniz <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocTableEvents.OnAfterAttributeChange%2A>.

Aşağıdaki örnek, bir kuramsal belge erişim senaryodur: Bir açık belgeler hakkında bazı bilgiler görüntülenecek uzantı istediği VisualStudio, örneği için Düzen kilit sayısı ve belge verilerini hakkında bir şey. Belgeleri kullanarak RDT numaralandırır <xref:Microsoft.VisualStudio.Shell.Interop.IEnumRunningDocuments>, sonra çağıran <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocumentTable.GetDocumentInfo%2A> düzenleme kilit sayısı ve belge verilerini almak için her belge için. Belge başlatma bekleyen durumda ise, belge verileri isteyen, gereksiz yere yeniden başlatılmasına neden olur.

Bir belgeye erişme daha verimli bir şekilde kullanmaktır <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocumentTable4.GetDocumentEditLockCount%2A> düzenleme kilit sayacını alın ve ardından <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocumentTable4.GetDocumentFlags%2A> belge başlatılmış olup olmadığını belirlemek için. Bayrakları dahil etmezseniz [_VSRDTFLAGS4. RDT_PendingInitialization](<xref:Microsoft.VisualStudio.Shell.Interop._VSRDTFLAGS4.RDT_PendingInitialization>), belge zaten başlatılmış ve belge verilerini ile isteyen <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocumentTable4.GetDocumentData%2A> gereksiz sıfırlamaları neden olmaz. Bayrakları dahil etmezseniz [_VSRDTFLAGS4. RDT_PendingInitialization](<xref:Microsoft.VisualStudio.Shell.Interop._VSRDTFLAGS4.RDT_PendingInitialization>), uzantıyı belge başlatılana kadar belge verileri isteyen kaçınmanız gerekir. Bu başlatma olarak algılanabilir `OnAfterAttributeChange(Ex)` olay işleyicisi.

## <a name="test-extensions-to-see-if-they-force-initialization"></a>Test başlatma zorla görmek için Uzantılar

Bir belge başlatılmış olup olmadığını, uzantınızı başlatma başlatılmasına gerek olmadığını bulmanın zor olabilir, böylece belirtmek için görünür hiçbir işaret yoktur. Metin tam olarak başlatılmadı her belgenin başlığını neden olduğundan doğrulama kolaylaştırır bir kayıt defteri anahtarı ayarlayabilirsiniz *[Stub]* başlık.

İçinde **HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\14.0\BackgroundSolutionLoad**ayarlayın **StubTabTitleFormatString** için  *{0} [Stub]* .