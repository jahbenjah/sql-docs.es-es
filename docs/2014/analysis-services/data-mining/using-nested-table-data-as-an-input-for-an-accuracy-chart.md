---
title: Usar datos de tabla anidada como entrada para un gráfico de precisión | Documentos de Microsoft
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- analysis-services
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Mining Accuracy Chart [Analysis Services], nested tables
- Mining Accuracy Chart [Analysis Services], input tables
- nested tables
- adding nested tables
ms.assetid: 162e0686-ada3-4dd3-9151-9589926e6613
caps.latest.revision: 23
author: Minewiskan
ms.author: owend
manager: mblythe
ms.openlocfilehash: 63f25ca15b3ce9cdf8c97a15f91d192ef6e7de96
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36108703"
---
# <a name="using-nested-table-data-as-an-input-for-an-accuracy-chart"></a>Usar datos de tabla anidada como entrada para un gráfico de precisión
  Al probar la precisión de un modelo de minería de datos usando datos externos, si el modelo de minería de datos contiene tablas anidadas, los datos externos también deben contener una tabla de casos y una tabla anidada asociada.  
  
 En este tema se describe cómo trabajar con las tablas anidadas que se usan para probar los modelos, cómo asignar tablas de casos y anidadas en el modo y en los datos externos, y cómo aplicar un filtro a una tabla anidada.  
  
 Al trabajar con tablas anidadas, tenga en cuenta estas sugerencias:  
  
-   Si selecciona la opción **Usar casos de prueba de modelo de minería de datos** o **Usar casos de prueba de estructura de minería de datos**, no es necesario que especifique una tabla de casos o una tabla anidada. Con estas opciones, la definición de los datos de prueba se almacena en la estructura de minería de datos y dichos datos se seleccionan automáticamente al crear el gráfico de precisión.  
  
-   Si ya existe una relación entre el caso y la tabla anidada en el origen de datos, las columnas de la estructura de minería de datos se asignan automáticamente a las columnas que tienen el mismo nombre en la tabla de entrada.  
  
-   No podrá seleccionar una tabla anidada hasta que haya especificado la tabla de casos. Tampoco podrá especificar una tabla anidada como entrada a menos que el modelo de minería de datos use también una estructura de tabla de casos y tabla anidada.  
  
### <a name="use-a-nested-table-as-input-to-an-accuracy-chart"></a>Utilice una tabla anidada como entrada para un gráfico de precisión  
  
1.  Haga doble clic en la estructura de minería de datos para abrirla en el Diseñador de minería de datos.  
  
2.  Seleccione la pestaña **Gráfico de precisión de minería de datos** y luego seleccione la pestaña **Selección de entrada** .  
  
3.  En **Seleccionar un conjunto de datos para usarlo en un gráfico de precisión**, seleccione la opción **Especificar otro conjunto de datos**.  
  
4.  Haga clic en el botón Examinar ( **…** ) para elegir el conjunto de datos externos en una lista de vistas del origen de datos del servidor actual.  
  
5.  Haga clic en **Seleccionar tabla de casos**. En el cuadro de diálogo **Seleccionar tabla** , elija la tabla en la vista del origen de datos que contiene los datos de los casos y, a continuación, haga clic en **Aceptar**.  
  
6.  Haga clic en **Seleccionar tabla anidada**. En el cuadro de diálogo **Seleccionar tabla** , seleccione la tabla que contiene los datos anidados y, a continuación, haga clic en **Aceptar**.  
  
7.  [!INCLUDE[clickOK](../../includes/clickok-md.md)]  
  
     Si tiene que modificar la relación entre la tabla anidada y la tabla de casos, haga clic en **Modificar combinación** para abrir el cuadro de diálogo **Crear relación** .  
  
## <a name="see-also"></a>Vea también  
 [Elegir y asignar el modelo de datos de prueba](choose-and-map-model-testing-data.md)   
 [Aplicar filtros a los datos de prueba del modelo](apply-filters-to-model-testing-data.md)  
  
  