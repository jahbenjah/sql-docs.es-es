---
title: Crear elemento (DTA) | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: tools-other
ms.topic: conceptual
dev_langs:
- XML
helpviewer_keywords:
- Create element (DTA)
ms.assetid: 9d076c90-f933-45f4-b6d9-447793f6528b
author: stevestein
ms.author: sstein
manager: craigg
ms.openlocfilehash: 7ec9ad9569326e4a9b3e890af4b5f909e36e5c5b
ms.sourcegitcommit: 334cae1925fa5ac6c140e0b2c38c844c477e3ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/13/2018
ms.locfileid: "53362197"
---
# <a name="create-element-dta"></a>Create (DTA, elemento)
  Contiene información sobre los índices, las estadísticas o las estructuras de montones de una configuración especificada por el usuario.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
<Recommendation>  
    <Create>  
    ...code removed here...  
    </Create>  
</Recommendation>  
```  
  
## <a name="element-characteristics"></a>Características de los elementos  
  
|Característica|Descripción|  
|--------------------|-----------------|  
|**Tipo y longitud de los datos**|Ninguno.|  
|**Valor predeterminado**|Ninguno.|  
|**Repetición**|Una obligatoria por cada tipo de estructura de diseño físico (índices, estadísticas o estructuras de montones).|  
  
## <a name="element-relationships"></a>Relaciones del elemento  
  
|Relación|Elementos|  
|------------------|--------------|  
|**Elemento primario**|[Elemento Recommendation &#40;DTA&#41;](recommendation-element-dta.md)|  
|**Elementos secundarios**|[Index &#40;DTA, elemento&#41;](index-element-dta.md)<br /><br /> `Statistics` Elemento (vea [esquema XML del Asesor de optimización de motor de base de datos](https://schemas.microsoft.com/sqlserver/) para obtener información)<br /><br /> `Heap` Elemento (vea [esquema XML del Asesor de optimización de motor de base de datos](https://schemas.microsoft.com/sqlserver/) para obtener información)|  
  
## <a name="remarks"></a>Comentarios  
 Este elemento tiene el nombre **CreateTypecomplexType** en el esquema XML del Asistente para la optimización de motor de base de datos. Se utiliza para crear los índices, las estadísticas y las estructuras de montones de una configuración especificada por el usuario. No confunda este elemento `Create` con los otros tipos que se pueden utilizar para crear vistas (`CreateViewType`) o particiones (`CreatePType`). Hacer referencia a la [esquema XML del Asesor de optimización de motor de base de datos](https://schemas.microsoft.com/sqlserver/) para obtener información acerca de los demás `Create` tipos de elemento.  
  
## <a name="example"></a>Ejemplo  
 Para obtener un ejemplo de uso de este elemento, vea [Ejemplo de archivo de entrada XML con configuración especificada por el usuario &#40;DTA&#41;](xml-input-file-sample-with-user-specified-configuration-dta.md).  
  
## <a name="see-also"></a>Vea también  
 [Referencia del archivo de entrada XML &#40;Asistente para la optimización de motor de base de datos&#41;](xml-input-file-reference-database-engine-tuning-advisor.md)  
  
  
