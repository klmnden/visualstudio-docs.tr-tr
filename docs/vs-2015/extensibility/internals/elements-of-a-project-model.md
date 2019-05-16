---
title: Proje modeli öğeleri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio SDK], implementation considerations
- project models
- projects [Visual Studio SDK], elements
ms.assetid: a1dbe0dc-68da-45d7-8704-5b43ff7e4fc4
caps.latest.revision: 19
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 0f3b07068939e34b5c9e9487761177c0e12f5654
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65700134"
---
# <a name="elements-of-a-project-model"></a>Proje Modeli Öğeleri
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Arabirimleri ve tüm projelerde uygulamaları [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] temel yapısını paylaşır: Proje türünüz için proje modeli. Geliştirdiğiniz VSPackage'ı olan proje modelinde tasarım kararlarınızı ile uyumlu ve IDE tarafından sağlanan genel işlevleri ile birlikte çalışan nesnelerin oluşturun. Örneğin, bir proje öğesi nasıl kalıcı denetim olsa da, bir dosya kalıcı gerekir bildirim kontrol edebilirim. Ne zaman bir kullanıcı bir açık proje öğesi üzerinde odağı yerleştirir ve seçer **Kaydet** üzerinde **dosya** menüsünde [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] menü çubuğu, proje türü kodunuzu gerekir IDE komuttan ıntercept, dosya kalıcı hale getirmek ve bildirimi, dosya artık değiştirildi IDE geri gönderin.  
  
 VSPackage, IDE arabirimlerine erişim sağladığı hizmetler aracılığıyla IDE ile etkileşime girer. Örneğin, belirli hizmetleri aracılığıyla, İzleyici ve rota komutları ve projede yapılan seçimleri bağlam bilgilerini sağlar. VSPackage'ı için gerekli tüm genel IDE işlevi, hizmetler tarafından sağlanır. Hizmetleri hakkında daha fazla bilgi için bkz. [nasıl yapılır: Hizmet alma](../../extensibility/how-to-get-a-service.md).  
  
 Diğer uygulama konuları:  
  
- Tek proje modeli, birden fazla proje türü içerebilir.  
  
- Proje türleri ve proje Katılımcısı fabrikaları GUID'lerini aşağıdaki ile bağımsız olarak kaydedilir.  
  
- Her proje, bir şablon dosyasında ya da kullanıcı yeni bir proje aracılığıyla oluşturduğunda, yeni proje dosyası başlatmak için Sihirbazı olmalıdır [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] kullanıcı Arabirimi. Örneğin, [!INCLUDE[vcprvc](../../includes/vcprvc-md.md)] şablonları başlatmak .vcproj dosyaları sonunda ne olur.  
  
  Aşağıdaki çizim, birincil arabirimleri, hizmetleri ve normal projesinin uygulaması oluşturan nesneleri gösterir. Uygulama Yardımcısı HierUtil7, temel alınan nesnelerin ve diğer programlama Demirbaş oluşturmak için kullanabilirsiniz. HierUtil7 uygulama Yardımcısı hakkında daha fazla bilgi için bkz: [derleme içinde değil: Bir proje türü (C++) uygulamak için HierUtil7 proje sınıflarını kullanarak](https://msdn.microsoft.com/a5c16a09-94a2-46ef-87b5-35b815e2f346).  
  
  ![Visual Studio Proje Modeli grafiği](../../extensibility/internals/media/vsprojectmodel.gif "vsProjectModel")  
  Proje modeli  
  
  Arabirimler ve önceki diyagramda listelenen hizmetlerin ve diyagramda yer almayan diğer isteğe bağlı arabirimler hakkında daha fazla bilgi için bkz. [proje modeli çekirdek bileşenleri](../../extensibility/internals/project-model-core-components.md).  
  
  Projeleri komutları destekleyebilir ve bu nedenle uygulamalıdır <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> komut içerikle GUID'leri komut yönlendirme de katılmak için arabirim.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yapılacaklar listesi: Yeni proje türleri oluşturma](../../extensibility/internals/checklist-creating-new-project-types.md)   
 [Derlemede değil: Bir proje türü (C++) uygulamak için HierUtil7 proje sınıflarını kullanma](https://msdn.microsoft.com/a5c16a09-94a2-46ef-87b5-35b815e2f346)   
 [Proje modeli çekirdek bileşenleri](../../extensibility/internals/project-model-core-components.md)   
 [Proje Üreteçlerini kullanarak proje örnekleri oluşturma](../../extensibility/internals/creating-project-instances-by-using-project-factories.md)   
 [Nasıl yapılır: Hizmet alma](../../extensibility/how-to-get-a-service.md)   
 [Proje Türleri Oluşturma](../../extensibility/internals/creating-project-types.md)
