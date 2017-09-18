---
title: ADCPROP_UPDATERESYNC_ENUM | Documentos de Microsoft
ms.prod: sql-non-specified
ms.technology:
- drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
apitype: COM
f1_keywords:
- ADCPROP_UPDATERESYNC_ENUM
helpviewer_keywords:
- ADCPROP_UPDATERESYNC_ENUM [ADO]
ms.assetid: bc9e1a37-e969-47e9-8382-0bbfffa2034f
caps.latest.revision: 11
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: e5c25ab6802b6a99902c9e52990be80ff14ed6d5
ms.contentlocale: es-es
ms.lasthandoff: 09/09/2017

---
# <a name="adcpropupdateresyncenum"></a>ADCPROP_UPDATERESYNC_ENUM
Especifica si el [UpdateBatch](../../../ado/reference/ado-api/updatebatch-method.md) método va seguido de un modo implícito [Resync](../../../ado/reference/ado-api/resync-method.md) operación del método y si es así, el ámbito de esa operación.  
  
|Constante|Valor|Description|  
|--------------|-----------|-----------------|  
|**adResyncAll**|15|Invoca **Resync** con el valor combinado de todos los demás miembros ADCPROP_UPDATERESYNC_ENUM.|  
|**adResyncAutoIncrement**|1|Predeterminado: Intenta recuperar el nuevo valor de identidad para las columnas que se incrementan automáticamente o generados por el origen de datos, como campos Autonuméricos de Microsoft Jet o las columnas de identidad de Microsoft SQL Server.|  
|**adResyncConflicts**|2|Invoca **Resync** para todas las filas en el que la operación update o delete no se pudo debido a un conflicto de simultaneidad.|  
|**adResyncInserts**|8|Invoca **Resync** para todas las filas insertadas correctamente. Sin embargo, los valores de columna de incremento automático no se vuelven a sincronizar. En su lugar, el contenido de las filas recién insertadas se vuelven a sincronizar según el valor de clave principal existente. Si la clave principal es un valor de incremento automático, **Resync** no recuperará el contenido de la fila prevista. Para incrementar automáticamente los valores de clave principal de incremento automático, llame a **UpdateBatch** con el valor combinado **adResyncAutoIncrement** + **adResyncInserts**.|  
|**adResyncNone**|0|No invocan **Resync**.|  
|**adResyncUpdates**|4|Invoca **Resync** para todas las filas se actualizó correctamente.|  
  
## <a name="applies-to"></a>Se aplica a  
 [Propiedad dinámica Update Resync (ADO)](../../../ado/reference/ado-api/update-resync-property-dynamic-ado.md)