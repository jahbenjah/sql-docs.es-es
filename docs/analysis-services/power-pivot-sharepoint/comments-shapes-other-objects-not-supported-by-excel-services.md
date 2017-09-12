---
title: Comentarios, formas, otros objetos no admitidos por Excel Services | Documentos de Microsoft
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- analysis-services
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: ade92e15-dfbf-496b-9378-a00bd83ba750
caps.latest.revision: 6
author: Minewiskan
ms.author: owend
manager: erikre
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: bb73f60aea4a67a2e7fe7967dc9411762fe8e8f9
ms.contentlocale: es-es
ms.lasthandoff: 09/01/2017

---
# <a name="comments-shapes-other-objects-not-supported-by-excel-services"></a>Comentarios, formas, otros objetos no admitidos por Excel Services
  Este error se produce al agregar segmentaciones a un libro [!INCLUDE[ssGemini](../../includes/ssgemini-md.md)] desde una lista de campos de [!INCLUDE[ssGemini](../../includes/ssgemini-md.md)] .  
  
## <a name="details"></a>Detalles  
  
|||  
|-|-|  
|Se aplica a|[!INCLUDE[ssGemini](../../includes/ssgemini-md.md)] para SharePoint|  
|Versión del producto|[!INCLUDE[ssKilimanjaro](../../includes/sskilimanjaro-md.md)], [!INCLUDE[ssSQL11](../../includes/sssql11-md.md)], [!INCLUDE[ssSQL14](../../includes/sssql14-md.md)]|  
|Causa|Excel Web Access no puede representar el objeto Forma que se usa para controlar la posición y el formato de las segmentaciones agregadas a un libro de la lista de campos de [!INCLUDE[ssGemini](../../includes/ssgemini-md.md)] .|  
|Texto del mensaje|Servicios de Excel no admite las siguientes características y puede que no se muestren o se muestren solo parcialmente:<br /><br /> Comentarios, formas o otros objetos<br /><br /> Algunas características, como las consultas de datos externos, muestran datos en caché que solo pueden actualizarse en Microsoft Excel.|  
  
## <a name="explanation"></a>Explicación  
 Excel Web Access muestra este error si abre un libro [!INCLUDE[ssGemini](../../includes/ssgemini-md.md)] en un explorador y hace clic en el botón **Detalles** para el mensaje **Características no admitidas. El libro probablemente no se muestre como está previsto**.  
  
 Este error se produce porque el libro [!INCLUDE[ssGemini](../../includes/ssgemini-md.md)] contiene segmentaciones cuyo diseño lo controla un objeto Forma oculto en Excel. El objeto Forma controla el formato y la posición de las segmentaciones en la posición horizontal y vertical.  
  
 Servicios de Excel no puede representar un objeto Forma, pero dado que el objeto está oculto, este hecho no constituye un problema.  
  
## <a name="user-action"></a>Acción del usuario  
 Se puede omitir este error. Haga clic en **Aceptar** para cerrar el mensaje de error y continuar utilizar el libro y las segmentaciones sin problema.  
  
  