---
title: Utilice la consulta y el Diseñador de vistas con datos internacionales (Visual Database Tools) | Documentos de Microsoft
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dbe-cross-instance
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Visual Database Tools [SQL Server], international data
- queries [SQL Server], international data
- languages [SQL Server], Query and View Designer
- international considerations [SQL Server], Query and View Designer
- Criteria pane
- View Designer, international data
- Query Designer [SQL Server], international data
- localized information in Query and View Designer [SQL Server]
- global considerations [SQL Server], Query and View Designer
- SQL pane [Visual Database Tools]
- multiple language support [SQL Server], Query and View Designer
ms.assetid: 4b51c56f-f902-4e72-b919-e36127369b63
caps.latest.revision: 10
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: 5ab3f1bbc7708b40243269724f949df4693dd488
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36112143"
---
# <a name="use-the-query-and-view-designer-with-international-data-visual-database-tools"></a>Utilizar el Diseñador de consultas y vistas con datos internacionales (Visual Database Tools)
  Puede usar el [Diseñador de consultas y vistas](visual-database-tools.md) con datos en cualquier idioma y en cualquier versión del sistema operativo Windows. Las siguientes instrucciones describen las diferencias que observará y proporcionan información sobre cómo administrar datos en aplicaciones internacionales.  
  
## <a name="localized-information-in-the-criteria-and-sql-panes"></a>Información localizada en los paneles Criterios y SQL  
 Si se está utilizando el panel Criterios para crear una consulta, los datos podrán especificarse en el formato que corresponda a la Configuración regional de Windows para el equipo. Por ejemplo, si está buscando datos, puede especificar los datos en las columnas Criterios mediante el uso de cualquier formato que esté acostumbrado a utilizar, con las siguientes excepciones:  
  
-   No se admiten formatos de datos largos.  
  
-   No deben especificarse símbolos de moneda en el panel Criterios.  
  
-   Los símbolos de moneda no se mostrarán en el panel Resultados.  
  
    > [!NOTE]  
    >  En el panel Resultados, puede especificar el símbolo de moneda que corresponda a la Configuración regional de Windows del equipo, pero el símbolo desaparecerá y no se mostrará en el panel Resultados.  
  
-   Un menos unario aparece siempre en el lado izquierdo (por ejemplo, -1), independientemente de las opciones de Configuración regional.  
  
 Por el contrario, los datos y palabras clave del panel SQL deberán estar siempre en formato ANSI (EE.UU.). Por ejemplo, a medida que el Diseñador de consultas y vistas genera una consulta, inserta la forma ANSI de todas las palabras clave SQL (por ejemplo, SELECT y FROM). Si agrega elementos a la instrucción en el panel SQL, asegúrese de utilizar la forma ANSI estándar para los elementos.  
  
 Al especificar datos mediante el uso de un formato regional específico en el panel Criterios, el Diseñador de consultas y vistas los traduce automáticamente a formato ANSI en el panel SQL. Por ejemplo, si la Configuración regional está establecida en Alemán (estándar), puede especificar datos en el panel Criterios en un formato como "31.12.96". Sin embargo, la fecha aparecerá en el panel SQL en formato de fecha y hora ANSI, como `{ ts '1996-12-31 00:00:00' }.` . Si escribe los datos directamente en el panel SQL, debe hacerlo en formato ANSI.  
  
## <a name="sort-order"></a>Criterio de ordenación  
 El criterio de ordenación de los datos de la consulta viene determinado por la base de datos. Las opciones que establece en el cuadro de diálogo Configuración regional de Windows no afectan al tipo de orden de las consultas. Sin embargo, en una consulta determinada puede solicitar que las filas se devuelvan en un orden concreto.  
  
## <a name="using-double-byte-characters"></a>Utilizar caracteres de doble byte  
 Puede especificar caracteres DBCS para literales y para nombres de objeto de base de datos tales como alias o nombres de vistas y tablas. También puede utilizar caracteres DBCS para nombres de parámetros y caracteres marcadores de parámetros. Sin embargo, no puede utilizar caracteres DBCS en elementos de lenguaje SQL tales como nombres de funciones o palabras clave SQL.  
  
## <a name="see-also"></a>Vea también  
 [Temas de procedimientos de diseño de consultas y vistas &#40;Visual Database Tools&#41;](design-queries-and-views-how-to-topics-visual-database-tools.md)  
  
  