---
title: Grafik olay listesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.graphics.eventlist
ms.assetid: a1252e19-b27d-4dc7-a16b-fdac894c1f0e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 710cc8cae2b1974529be1eded6c5148eedd1211e
ms.sourcegitcommit: 283f2dbce044a18e9f6ac6398f6fc78e074ec1ed
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/16/2019
ms.locfileid: "65805309"
---
# <a name="graphics-event-list"></a>Grafik Olay Listesi
Grafik olay listesi oyunlarda veya uygulamalarda karesi işlenirken kaydedilmiş Direct3D olayları keşfetmek için Visual Studio grafik Çözümleyicisi'nde kullanın.

 Bu olay listesi.

 ![Adında "Index" olan olaylar listesi. ](media/gfx_diag_demo_event_list_orientation.png "gfx_diag_demo_event_list_orientation")

## <a name="using-the-event-list"></a>Olay listesi kullanma
 Olay listesi, bunu diğer grafik analizi araçları tarafından görüntülenen bilgileri yansıtılan bir olay seçtiğinizde, Bu diğer araçlar ile uyumlu bir şekilde olay listesi kullanılarak bir işleme sorunun nedenini belirlemek için ayrıntılı inceleyebilirsiniz. Olay listesi diğer grafik analizi araçları ile birlikte kullanarak işleme sorunları nasıl çözebileceğiniz hakkında daha fazla bilgi için bkz: [örnekler](graphics-diagnostics-examples.md).

 Olay listesi özelliklerinin etkili bir şekilde kullanarak, binlerce olayın içerebilir karmaşık çerçevelerinin çevresinde almak için önemlidir. Olay listesi verimli bir şekilde kullanma, görünüm sizin için en uygun seçin, arama olay listesini filtrelemek için bir olayla ilişkili olan Direct3D nesneleri hakkında daha fazla bilgi edinmek için bağlantıları izleyin ve oku çağrıları arasında taşımak için düğmeler hızla çizin.

### <a name="color-coded-events-in-direct3d-12"></a>Direct3D 12 renk kodlu olaylar
 Direct3D 12 farklı donanım işlevselliği için karşılık gelen birden fazla kuyruk kullanıma sunar. Bir Direct3D 12 uygulama yakalama ile çalışırken, bir Direct3D 12 belirli grafik olay ile ilişkili kuyruk belirlemenize yardımcı olması için olayları Olay listesindeki kendi sıra göre renk kodludur.

|Direct3D 12 sırası|Renk|
|-----------------------|-----------|
|Kuyruk oluştur|Yeşil|
|Kuyruk işlem|Sarı|
|Kopyalama kuyruğu|Turuncu|

 Direct3D 11 birden fazla kuyruk kullanıma sunmak değil, Direct3D 11 uygulamasının bir yakalama ile çalışırken olayları renk kodlu kalmayacak bir olay listesi.

### <a name="event-list-views"></a>Olay liste görünümleri
 Olay listesi, grafik olaylarını düzenleme iş akışı ve tercihlerinizi desteklemek için farklı şekilde iki farklı görünümleri destekler. İlk görünümdür *GPU iş görünümü* hangi düzenler olayları ve durumlarını ilişkili hiyerarşik olarak. İkinci görünüm *zaman çizelgesi görünümü* hangi düzenler olayların kronolojik, düz bir liste.

 **GPU işi** görüntüler yakalanan olayları ve durumlarını bir hiyerarşide görünümü. Hiyerarşinin üst düzey olayları gibi çizim çağrıları, temizler, mevcut ve görünümler ile de oluşur. Olay listesi, çizim çağrılarını çizim çağrısı zaman güncel olan cihaz durumunu görüntülemek için genişletebilirsiniz; ve her tür değerlerini belirleyen olayları görüntülemek için durumları daha da genişletebilirsiniz. Bu düzey, önceki bir çerçeve içinde belirli bir duruma ayarlanmış olup olmadığını ya da son çizim çağrısı bu yana kereden fazla ayarlandı da görebilirsiniz.

 **Zaman çizelgesi** görünüm kronolojik sırayla her yakalanan olay görüntüler. Olay listesi düzenleme bu şekilde Visual Studio'nun önceki sürümlerinde olduğu gibi aynı olur.

##### <a name="to-change-the-event-list-view-mode"></a>Olay listesi görünümü modu değiştirmek için

- İçinde **grafik olay listesi** penceresinde, olayların listesinin üst bulun **görünümü** açılır ve seçeneğini **zaman çizelgesi** görünümü veya **GPUişi** görünümü.

### <a name="filtering-events"></a>Olayları filtreleme
 Arama kutusunu kullanabilirsiniz — sağ üst köşesinde bulunan **grafik olay listesi** penceresi — yalnızca adında belirli anahtar sözcükler olayları dahil etmek için olayları listeyi filtrelemek için. İster tek anahtar sözcükleri belirtebilirsiniz `Vertex`— önceki resimde gösterildiği gibi — veya noktalı virgülle ayrılmış bir liste kullanarak birden çok anahtar sözcükleri `Draw;Primitive`— ya da sahip olayları eşleşen `Draw` veya `Primitive` adlarında. Aramalar için boşluk hassas — Örneğin, `VSSet` ve `VS Set` farklı aramalar — böylece form aramaları için dikkatli bir şekilde sağlayın.

### <a name="moving-between-draw-calls"></a>Çizim çağrıları arasında taşıma
 İnceleme çünkü `Draw` çağrıdır kullanabileceğiniz özellikle önemli **sonraki Git çizim çağrısı** ve **Git önceki çizim çağrısı** düğmeleri — solüstköşesindebulunan**Grafik olay listesi** penceresi — bulup çizim çağrıları arasında kolayca taşıyın.

### <a name="links-to-graphics-objects"></a>Grafik nesneleri bağlantılar
 Belirli grafik olaylarını anlamak için bir olay tarafından başvurulan Direct3D nesneleri veya Direct3D geçerli durumu hakkında ek bilgi gerekebilir. Çok sayıda olay daha fazla ayrıntı için izleyebileceğiniz bu bilgilere bağlantılar sağlar.

## <a name="kinds-of-events-and-event-markers"></a>Olaylar ve olay işaretçileri tür
 Liste düzenlenir olay dört kategoriye görüntülenen olayları: genel olaylar, olaylar, olay kullanıcı tanımlı grupları ve kullanıcı tanımlı olay işaretçileri çizin. Genel olaylar dışında her olay ait olduğu kategoriyi belirten bir simge ile birlikte görüntülenir.

|Simge|Olay açıklaması|
|----------|-----------------------|
|(simge yok)|Genel olay<br /> Değil kullanıcı tanımlı olay, kullanıcı tanımlı olay grubu veya olay çizmek herhangi bir olay.|
|![Çizim olay simgesi](media/vsg_eventlist_icon_draw.png "vsg_eventlist_icon_draw")|Çizim olayından<br /> Yakalanan karede bir çizim olayından işaretler.|
|![Kullanıcı&#45;olay işaret simgesi tanımlanan](media/vsg_eventlist_icon_user.png "vsg_eventlist_icon_user")|Kullanıcı tanımlı olay grubu<br /> Grupları, uygulama tarafından tanımlanan olayları, ilgili.|
|![Kullanıcı&#45;olay işaret simgesi tanımlanan](media/vsg_eventlist_icon_user.png "vsg_eventlist_icon_user")|Kullanıcı tanımlı olay işaretçisi<br /> Belirli bir konuma uygulama tarafından tanımlanan olarak işaretler.|

## <a name="marking-user-defined-events-in-your-app"></a>Uygulamanızda işaretlenmesi kullanıcı tanımlı olayları
 Kullanıcı tanımlı olaylar, uygulamanıza özgü niteliktedir. Grafik olay listesi olayları ile uygulamanızda gerçekleşen önemli olayları ilişkilendirmek için bunları kullanabilirsiniz. Örneğin, ilgili olaylar düzenlemek için kullanıcı tanımlı olay gruplar oluşturabilirsiniz — Bu, kullanıcı arabirimini oluşturmak gibi — olay listesi daha kolayca göz atabilir veya belirli bir türdeki nesneler, işaretçileri oluşturabilirsiniz böylece grupları veya Hiyerarşiler olan çizilen. böylece, grafik olaylarını Olay listesi kolayca bulabilirsiniz.

 Gruplar ve işaretçileri, uygulamanızı oluşturmak için diğer Direct3D tarafından hata ayıklama araçları kullanmak için Direct3D sağlayan API'leri kullanın. Bu API'ler, bazen Direct3D sürümleri arasında değiştirmek, ancak temel işlevleri aynıdır.

### <a name="user-defined-events-in-direct3d-12"></a>Kullanıcı tanımlı olayları, Direct3D 12
 Direct3D 12'deki gruplar ve işaretçileri oluşturmak için bu bölümde açıklanan API'leri kullanın. Aşağıdaki tabloda, bir komut kuyruğuna olaylar işaretleme veya liste komut bağlı olarak kullanabileceğiniz API'ler özetler.

|API tanımı|[ID3D12CommandQueue](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue)|[ID3D12GraphicsCommandList](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)|
|---------------------| - | - |
|Kullanıcı tanımlı olay kullanılabilirliğini denetle|[PIXGetStatus](/previous-versions//dn788637(v=vs.85))|[PIXGetStatus](/previous-versions//dn788637(v=vs.85))|
|Olay grubu başlayın|[PIXBeginEvent](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent)|[PIXBeginEvent](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent)|
|Son olay grubu|[PIXEndEvent](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-endevent)|[PIXEndEvent](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent)|
|Bir olay işaretçisi oluşturma|[PIXSetMarker](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker)|[PIXSetMarker](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker)|

### <a name="user-defined-events-in-direct3d-11-and-earlier"></a>Direct3D 11'de ve önceki kullanıcı tanımlı olayları
 Grupları ve Direct3D 11 veya önceki işaretçileri oluşturmak için bu bölümde açıklanan API'leri kullanın. Aşağıdaki tabloda farklı sürümlerini Direct3D 11 ve Direct3D önceki sürümleri için kullanabileceğiniz API'ler özetler.

|API tanımı|[ID3D11DeviceContext2](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) (Direct3D 11.2)|[ID3DUserDefinedAnnotation](http://go.microsoft.com/fwlink/p/?LinkID=250967) (Direct3D 11.1)|D3DPerf_ API ailesi (Direct3D 11.0 ve daha önceki)|
|---------------------| - | - | - |
|Olay grubu başlayın|`BeginEventInt`|`BeginEvent`|`D3DPerf_BeginEvent`|
|Son olay grubu|`EndEventInt`|`EndEvent`|`D3DPerf_EndEvent`|
|Bir olay işaretçisi oluşturma|`SetMarkerInt`|`SetMarker`|`D3DPerf_SetMarker`|

 Direct3D sürümünüz destekleyen bu API dilediğinizi kullanabilirsiniz — Direct3D 11.1 API hedefliyorsanız, örneğin, kullanabilirsiniz `SetMarker` veya `D3DPerf_SetMarker` bir olay işaretçisi değil oluşturmak için `SetMarkerInt` çünkü Direct3D, yalnızca kullanılabilir 11.2 — ve Direct3D'ün farklı sürümlerini birlikte aynı uygulamada destekleyen olanlar bile karıştırabilirsiniz.

<!-- VERSIONLESS -->
<a name="resource-history"></a>
## <a name="resource-history"></a>Kaynak geçmişi
Visual Studio 2017 ve daha sonraki sürümleri içeren **kaynak geçmişi** penceresi.  İzle simgesini seçerek ![izleme simgesi](media/gfx_watch.png) bir girişi yanındaki **olay listesi** pencere ortaya çıkarmak **kaynak geçmişi** aşağıda gösterilen penceresi:

![Kaynak geçmişi](media/gfx_diag_resource_history.png)

Bu pencere, olay listedeki seçili öğenin geçmişini görüntülemek sağlar.  Üstteki açılan geçmişini görüntülemek için diğer öğeleri seçmek için kullanılabilir.  Pencerenin üst kısmında içeren **çerçeve Kurulumu olayları**.  Bunlar yer alacağı olayları *Oluştur* kategori yazın ve genellikle başlatmak ve kaynak oluşturma çağrıları.  Pencerenin yarısını içeren alt **çerçeve olayları** bölümü.  Bunlar normal okuma ve yazma sırasında kaynak kullanımını meydana gelen olayları.

| Sütun | Açıklama |
|-----------| - |
| **Tür** | Giriş türü genellikle gösterilir *Oluştur*, *okuma* ve *yazma*. |
| **Görünümü** | Zaman içinde o anda bir küçük resim kaynağının adını gösterir.  Küçük resim o anda bir kaynak Ayrıntıları görünümünü açmak için çift tıklayın. |
| **Event** | Oluştuğu yöntem çağrısının gösterir olay oluşturulur.  Bireysel öğeleri üzerinde başka bir geçmiş İzle simgesini seçerek görüntülenebilir ![izleme simgesi](media/gfx_watch.png) uygun satırda.  Ayrıca, mavi renkte gibi çizilir hiçbir öğe `m_commandList` daha fazla ayrıntı için yukarıdaki ekran görüntüsünde, seçilebilir. |

<!-- /VERSIONLESS -->

## <a name="see-also"></a>Ayrıca Bkz.
- [İzlenecek yol: Cihaz Durumu Nedeniyle Eksik Nesneler](walkthrough-missing-objects-due-to-device-state.md)