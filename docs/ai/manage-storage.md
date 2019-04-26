---
title: Verileri karşıya yüklemeye, depolamaya Gözat
author: lisawong19
ms.author: liwong
manager: routlaw
ms.date: 11/13/2017
ms.topic: conceptual
ms.workload:
- multiple
ms.openlocfilehash: 8990252f78a9e89b9bdaa825d5443e4d38d2ae89
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62548238"
---
# <a name="browse-storage-to-upload-data-or-download-models-and-logs"></a>Karşıya veri yükleme veya modelleri ve günlükleri indirmek için depolamaya Gözat

Uzak makinede veya karşıya yükleme verileri veya yükleme modelleri ve günlükleri etkinleştirmek için Azure dosya paylaşımı tüm depolama göz atabilirsiniz. Ya da günlükleri ve belirli bir işin iş çıktıları erişmek istiyorsanız, bunu da iş tarayıcıda yapabilirsiniz.

## <a name="to-access-all-data-on-the-remote-machine-or-file-share"></a>Uzaktan kumandanın tüm verilere erişmek için makine veya dosya paylaşımından

1. Açık **Sunucu Gezgini**.
2. Uzak makine ya da işlem bağlamını Batch AI'ı genişletin.
3. Sağ **depolama**;'a tıklayarak **Gözat**.

    ![depolama](media/manage-storage/browse-storage.png)

## <a name="to-access-job-specific-data-on-the-remote-machine-or-file-share"></a>Uzak iş özel verilere erişmek için makine veya dosya paylaşımından

1. Açık [iş geçmişi](job-details.md)
2. İşi seçin.
3. Tıklayın **çalışma klasörü** veya **StdOut / Stderr** hızlı erişim için bu önemli bir günlük dosyaları.

    ![depolama](media/manage-storage/job-workingfolder.png)