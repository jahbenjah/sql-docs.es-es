---
title: Sys.pdw_health_alerts (Transact-SQL) | Documentos de Microsoft
ms.custom: 
ms.date: 03/03/2017
ms.prod: sql-non-specified
ms.prod_service: pdw
ms.service: 
ms.component: system-catalog-views
ms.reviewer: 
ms.suite: sql
ms.technology: database-engine
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 49c01e5f-ee47-41a0-871d-35a759f50851
caps.latest.revision: "7"
author: barbkess
ms.author: barbkess
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 0f7e05ccc9cc264faf5d4d7f563d1df028969309
ms.sourcegitcommit: 44cd5c651488b5296fb679f6d43f50d068339a27
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2017
---
# <a name="syspdwhealthalerts-transact-sql"></a>Sys.pdw_health_alerts (Transact-SQL)
[!INCLUDE[tsql-appliesto-xxxxxx-xxxx-xxxx-pdw-md](../../includes/tsql-appliesto-xxxxxx-xxxx-xxxx-pdw-md.md)]

  Almacena las propiedades para las alertas diferentes que se pueden producir en el sistema; se trata de una tabla de catálogos para las alertas.  
  
|Nombre de la columna|Tipo de datos|Description|Intervalo|  
|-----------------|---------------|-----------------|-----------|  
|alert_id|**int**|Identificador único de la alerta.<br /><br /> Clave para esta vista.|NOT NULL|  
|IdComponente|**int**|Id. del componente al que se aplica esta alerta. El componente es un identificador de componente general, por ejemplo, "Alimentación" y no es específico para una instalación. Vea [sys.pdw_health_components &#40; Transact-SQL &#41; ](../../relational-databases/system-catalog-views/sys-pdw-health-components-transact-sql.md).|NOT NULL|  
|alert_name|**nvarchar(255)**|Nombre de la alerta.|NOT NULL|  
|state|**nvarchar (32)**|Estado de la alerta.|NOT NULL<br /><br /> Valores posibles:<br /><br /> 'Operational'<br /><br /> 'No operativa'<br /><br /> 'Degradado'<br /><br /> "Error"|  
|severity|**nvarchar (32)**|Gravedad de la alerta.|NOT NULL<br /><br /> Valores posibles:<br /><br /> 'Informativo'<br /><br /> 'Advertencia'<br /><br /> 'Error'|  
|Tipo|**nvarchar (32)**|Tipo de alerta.|NOT NULL<br /><br /> Valores posibles:<br /><br /> StatusChange - ha cambiado el estado del dispositivo.<br /><br /> Umbral - un valor ha superado el valor de umbral.|  
|description|**nvarchar(4000)**|Descripción de la alerta.|NOT NULL|  
|condición|**nvarchar(255)**|Utiliza cuando escriba = umbral. Define cómo se calcula el umbral de alerta.|NULL|  
|status|**nvarchar (32)**|Estado de alerta|NULL|  
|condition_value|**bit**|Indica si la alerta se permite que se produzca durante la operación del sistema.|NULL<br /><br /> Valores posibles<br /><br /> 0 - no se generará la alerta.<br /><br /> 1 - la alerta se genera.|  
  
## <a name="see-also"></a>Vea también  
 [Almacenamiento de datos SQL y vistas de catálogo del almacén de datos en paralelo](../../relational-databases/system-catalog-views/sql-data-warehouse-and-parallel-data-warehouse-catalog-views.md)  
  
  