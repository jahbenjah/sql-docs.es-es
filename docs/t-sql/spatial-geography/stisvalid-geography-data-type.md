---
title: STIsValid (tipo de datos geography) | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: t-sql
ms.topic: language-reference
dev_langs:
- TSQL
helpviewer_keywords:
- STIsValid method (geography)
ms.assetid: 1bfe787f-ddf0-4fc7-af6a-570a58faab23
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: cceede70a5458abe72d6659312d897d7b68bb086
ms.sourcegitcommit: 61381ef939415fe019285def9450d7583df1fed0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2018
ms.locfileid: "47774983"
---
# <a name="stisvalid-geography-data-type"></a>STIsValid (tipo de datos geography)
[!INCLUDE[tsql-appliesto-ss2012-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2012-asdb-xxxx-xxx-md.md)]

  Devuelve true si una instancia de **geography** tiene el formato correcto y está reconocida como un objeto de geografía válido basado en su tipo OGC (Open Geospatial Consortium). Devuelve false si una instancia de **geography** no tiene el formato correcto. Este método es preciso.  
  
 Este método del tipo de datos geography admite instancias de **FullGlobe** o instancias espaciales mayores que un hemisferio.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
.STIsValid ( )  
```  
  
## <a name="return-types"></a>Tipos devueltos  
 Tipo de valor devuelto de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]: **bit**  
  
 Tipo de valor devuelto de CLR: **SqlBoolean**  
  
## <a name="remarks"></a>Notas  
 El tipo OGC de una instancia de **geography** se puede determinar mediante la invocación de [STGeometryType()](../../t-sql/spatial-geography/stgeometrytype-geography-data-type.md).  
  
 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] solo produce instancias válidas de **geography**, pero permite el almacenamiento y la recuperación de instancias no válidas. El método `MakeValid()` permite recuperar una instancia válida que representa el mismo conjunto de puntos de una instancia no válida.  
  
## <a name="examples"></a>Ejemplos  
 En el ejemplo siguiente se crea una instancia de `geography` y se usa `STIsValid()` para comprobar si dicha instancia es válida.  
  
```  
DECLARE @g geography = geography::STGeomFromText('LINESTRING(0 0, 2 2, 1 0)', 4326);  
SELECT @g.STIsValid();  
DECLARE @g geography  
```  
  
## <a name="see-also"></a>Ver también  
 [STGeometryType &#40;tipo de datos geography&#41;](../../t-sql/spatial-geography/stgeometrytype-geography-data-type.md)   
 [MakeValid &#40;tipo de datos geography&#41;](../../t-sql/spatial-geography/makevalid-geography-data-type.md)   
 [Métodos de OGC en instancias de geography](../../t-sql/spatial-geography/ogc-methods-on-geography-instances.md)  
  
  
