---
title: Grafik Çerçeve doğrulama | Microsoft Docs
ms.date: 03/02/2017
ms.topic: conceptual
f1_keywords:
- vs.graphics.FrameValidation
ms.assetid: 1e639182-1301-4e28-9c1e-b5df732f3f1b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b353954f56cc71922d1ec5e7aef483c7bad2f47f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54991534"
---
# <a name="graphics-frame-validation"></a>Grafik Çerçeve doğrulama
<!-- VERSIONLESS --> Visual Studio 2017 ve daha büyük Destek **çerçeve doğrulama** aracı.  Çerçeve doğrulama penceresi, hataları ve olay listesi ile ilişkili uyarıları görüntüler.  Bu pencereyi görüntülemek için seçin **Görüntüle > Çerçeve doğrulama** menüsü.

![Çerçeve Doğrulama](media/gfx_diag_frame_validation.png)

Tıklayın **doğrulama çalışması** analiz başlatmak için sol üst köşedeki düğmesini.  Bu çerçeve karmaşıklığına bağlı olarak tamamlanması birkaç dakika sürebilir.  İki farklı kaynaktan gelen bir birleşimini aşağıdadır görüntülenen verileri: iletileri bu D3D kendisini ne zaman yayar [SDK katmanları](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers) etkinleştirilmiş ve İzleme Aracı'nın kendi iç durumu toplanan verileri. İşlem tamamlandıktan sonra birkaç veri sütunlarının görürsünüz:


| **Sütun** | **Açıklama** |
|------------| - |
| Olay Kimliği | İçindeki bir girdiye eşleştiren kimliği [olay listesi](graphics-event-list.md) penceresi. |
| Önem Derecesi | Bozulma, hata, uyarı, bilgi veya ileti. |
| Kategori | Tanımlanmış, çeşitli uygulama başlatma, temizleme, derleme, durum oluşturma, durumu ayarı, durum alma, yürütme, kaynak düzenlemesi, gölgelendirici, gereksiz ve kullanılmayan. |
| İleti | Olayla ilişkili ileti. |
| Olay | Hata veya uyarı ile ilişkili olay. |

## <a name="see-also"></a>Ayrıca Bkz.  
[Grafik tanılama (DirectX grafik hata ayıklama)](visual-studio-graphics-diagnostics.md)   
<!-- /VERSIONLESS -->