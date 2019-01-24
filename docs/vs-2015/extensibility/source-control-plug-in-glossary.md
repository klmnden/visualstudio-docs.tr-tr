---
title: Kaynak Denetimi Eklentisi sözlüğü | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- glossary [Visual Studio SDK]
- source control plug-ins, glossary
ms.assetid: f224bbc9-38fc-4c80-ab09-51dcc8969f8e
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: f5120a5c6678cac32ef65e08ef7dc34649364cf9
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54776563"
---
# <a name="source-control-plug-in-glossary"></a>Kaynak Denetimi Eklentisi Sözlüğü
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Aşağıdaki yardımcı terimleri ve tanımları kaynak denetimi eklentisi SDK belgelerine ilgilidir.  
  
## <a name="definitions"></a>Tanımlar  
 İade etme  
 Bir kullanıcı için çalışan bir kopya değişiklik yaptığında, bir kullanıcı merkezi kaynak denetim deposu ile çalışma kopyadan değişiklikleri göndermeniz gerekir. Bu, diğer kullanıcılar için kullanılabilir olan dosyayı yeni bir düzeltmesi oluşturulur. Bu işlem, bir iade etme denir.  
  
 Kullanıma alma  
 Bir çalışma kopyası amacınızla değiştirmek için depoyu bildiren depodan isteme işlemi. Bir çalışan kopya kullanıma andan itibaren proje durumunu yansıtır.  
  
 İstemci  
 Kaynak kod denetim sistemini kullanan bir program. Bu belgede, bu Visual Studio IDE olur.  
  
 Yorum  
 Kaynak denetimi işlemi gerçekleştirilirken bir kullanıcı için bir düzeltme ekleyebilirsiniz değişiklikleri açıklayan bir ileti.  
  
 Çakışma  
 İki kullanıcı aynı bölgede aynı dosyasının değişiklikleri iade çalıştığınızda bir durumdur. Genellikle, bir birleştirme gerçekleştirilmelidir.  
  
 Dizin  
 İstemci tarafı yerel bir klasöre bir dizin adlandırılır. Bu, bir kullanıcının değişiklikleri gerçekten yaptığı kopyasıdır. Belirli bir projenin birçok çalışma kopyalarının olabilir; genellikle her geliştirici kendi kopya vardır.  
  
 Al  
 Bir Al işlemi, kullanıcının çalışma kopyası güncel depo kopyalama ile getirir. Kullanıcı yalnızca en son kopyasını gerekiyor ancak değişiklik amaçlayan bir kullanıma alma, bir get gerçekleştirilir.  
  
 Geçmiş  
 Buna genellikle bir özetini tüm kullanıma alma, iadeler, güncelleştirmeleri, etiketler ve kaynak denetim deposunda bitti yayınlar var.  
  
 IDE  
 Genel olarak, Visual Studio tümleşik geliştirme ortamı için ifade eder. Ancak, kaynak denetimi eklentisi API tanımak diğer istemci ortamları da başvurabileceğiniz.  
  
 Birleştir  
 İşlem sırasında hangi iki veya daha fazla kaynak kod dosyaları önceki dosyalarından tüm özellikleri içerir, yeni bir dosya oluşturmak üzere birleştirilir. Bu kavramı burada iki veya daha fazla geliştiriciler dosyalar üzerinde eşzamanlı olarak çalışabilir sürüm denetiminde önemlidir.  
  
 Proje  
 Bir kaynak denetim klasörünü, genellikle bir proje olarak da adlandırılır. Visual Studio'da bu projeler veya çözümler ile hiçbir ilişkisi yok.  
  
 Eklenti  
 DLL kaynak denetimi eklentisi API uygulayarak kaynak denetimi işlevlerini sağlar.  
  
 Havuz  
 Burada bir kaynak denetim sistemi ana kopya bir projenin tam düzeltme geçmişi saklar. Her projenin tam olarak bir depo yok.  
  
 Gözden geçirme  
 Bir dosyanın geçmişini veya dosya kümesini edilen bir değişikliği. Bir düzeltme biridir sürekli olarak değişen bir projede anlık görüntüsünü alın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentileri](../extensibility/source-control-plug-ins.md)
