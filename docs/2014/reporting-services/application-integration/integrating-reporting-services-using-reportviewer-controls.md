---
title: Integrar Reporting Services con los controles ReportViewer | Microsoft Docs
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology:
- docset-sql-devref
- reporting-services-native
ms.topic: reference
helpviewer_keywords:
- ReportViewer controls
- integrating reports [Reporting Services]
ms.assetid: 3ba47fb4-73a9-4059-89fd-329adebe94a8
author: markingmyname
ms.author: maghan
manager: kfile
ms.openlocfilehash: cf09c6f06cbdb4e24949ad1f078312869c81444d
ms.sourcegitcommit: aa4f594ec6d3e85d0a1da6e69fa0c2070d42e1d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2019
ms.locfileid: "59241643"
---
# <a name="integrating-reporting-services-using-the-reportviewer-controls"></a>Integrar Reporting Services con los controles ReportViewer
  [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[vsOrcas](../../includes/vsorcas-md.md)] provides two ReportViewer controls for integratingproporciona dos controles ReportViewer para integrar la funcionalidad de visualización de informes en las aplicaciones.aHay una versión para las aplicaciones basadas en formularios Windows Forms y otra para las aplicaciones de formularios Web Forms.aCada control proporciona una funcionalidad similar, pero cada uno está diseñado para sus entornos individuales.dAmbos controles pueden procesar los informes que se hayan implementado en un servidor de informes (modo de procesamiento remoto) o se hayan copiado en un equipo donde no se haya instalado [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] (modo de procesamiento local).  
  
 El control ReportViewer no incluye compatibilidad integrada para adaptarse dinámicamente a distintos dispositivos con diferentes resoluciones de pantalla.  
  
## <a name="remote-processing-mode"></a>Modo de procesamiento remoto  
 El modo del procesamiento remoto es el método preferido para ver los informes implementados en un servidor de informes. El modo de procesamiento remoto proporciona las ventajas siguientes:  
  
-   El procesamiento remoto proporciona una solución optimizada para ejecutar informes porque el servidor de informes los procesa.  
  
-   Dado que el servidor de informes controla todo el procesamiento, en una implementación escalada, varios servidores de informes pueden procesar una solicitud de informe o bien, en un escenario de ampliación de la capacidad, puede procesarla un servidor que tenga varios procesadores.  
  
 Además, los informes que se ejecutan en modo remoto pueden utilizar la funcionalidad completa del servidor de informes incluidas todas las extensiones de datos y de representación.  
  
> [!NOTE]  
>  La lista de extensiones disponibles para el control ReportViewer cuando se ejecuta en modo de procesamiento remoto depende de la edición de [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] que esté instalada en el servidor de informes.  
  
## <a name="local-processing-mode"></a>Modo de procesamiento local  
 El modo de procesamiento local proporciona un método alternativo para ver y representar los informes cuando [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] no está instalado. A diferencia del procesamiento remoto, en el control solo está disponible un subconjunto de la funcionalidad que proporciona el servidor de informes. En el modo de procesamiento local, el control no administra el procesamiento de los datos sino que se implementa mediante la aplicación de host. Pero el propio control controla el procesamiento de informes. En el modo de procesamiento local, solo están disponibles las extensiones de representación PDF, Excel, Word e Image.  
  
## <a name="see-also"></a>Vea también  
 [Integrar Reporting Services en las aplicaciones](../application-integration/integrating-reporting-services-into-applications.md)   
 [Crear informes SSRS mediante Visual Studio (Blog)](https://jwcooney.com/2015/01/07/ssrs-basics-set-up-visual-studio-to-write-a-new-ssrs-report/)  
  
  
