---
title: Mostrar valores de porcentaje en un gráfico circular (Generador de informes y SSRS) | Microsoft Docs
ms.date: 03/01/2017
ms.prod: reporting-services
ms.prod_service: reporting-services-sharepoint, reporting-services-native
ms.technology: report-design
ms.topic: conceptual
ms.assetid: eb905fc1-5235-4773-a27e-b07be9318be5
author: markingmyname
ms.author: maghan
ms.openlocfilehash: bbc386708543b82fd79c012a40ab94f8001f5815
ms.sourcegitcommit: 31800ba0bb0af09476e38f6b4d155b136764c06c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2019
ms.locfileid: "56289823"
---
# <a name="display-percentage-values-on-a-pie-chart-report-builder-and-ssrs"></a>Mostrar valores de porcentaje en un gráfico circular (Generador de informes y SSRS)
En informes paginados de [!INCLUDE[ssRSnoversion_md](../../includes/ssrsnoversion-md.md)], de forma predeterminada, la leyenda muestra las categorías. Es posible que también quiera ver porcentajes en la leyenda o los propios segmentos del gráfico circular.   

![report-builder-pie-chart-preview-percents](../../reporting-services/media/report-builder-pie-chart-preview-percents.png)

 El [Tutorial: Agregar un gráfico circular a un informe (generador de informes)](Tutorial:%20Add%20a%20Pie%20Chart%20to%20Your%20Report%20\(Report%20Builder\).md) le guía a lo largo del proceso de agregar porcentajes a segmentos del gráfico circular, si primero quiere probar esto con datos de ejemplo.
 
  
## <a name="to-display-percentage-values-as-labels-on-a-pie-chart"></a>Para mostrar los valores de porcentaje como etiquetas en un gráfico circular  
  
1.  Agregue un gráfico circular al informe. Para más información, vea [Agregar un gráfico a un informe &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/add-a-chart-to-a-report-report-builder-and-ssrs.md).  
  
2.  En la superficie de diseño, haga clic con el botón derecho en gráfico circular y seleccione **Mostrar etiquetas de datos**. Las etiquetas de datos aparecerán dentro de cada sector del gráfico circular.  
  
3.  En la superficie de diseño, haga clic con el botón secundario en las etiquetas y seleccione **Propiedades de la etiqueta de la serie**. Aparece el cuadro de diálogo **Propiedades de la etiqueta de la serie** .  
  
4.  Escriba **#PERCENT** para la opción **Datos de etiqueta** .  
  
5.  (Opcional) Para especificar el número de posiciones decimales que se deben mostrar en la etiqueta, escriba "#PERCENT{P*n*}", donde *n* es el número de posiciones decimales que se deben mostrar. Por ejemplo, para no mostrar ninguna posición decimal, escriba "#PERCENT{P0}".  
  
## <a name="to-display-percentage-values-in-the-legend-of-a-pie-chart"></a>Para mostrar los valores de porcentaje en la leyenda de un gráfico circular  
  
1.  En la superficie de diseño, haga clic con el botón secundario en el gráfico circular y seleccione **Propiedades de la serie**. Aparece el cuadro de diálogo **Propiedades de la serie** .  
  
2.  En **Leyenda**, escriba **#PERCENT** para la propiedad **Texto de leyenda personalizado** .  
  
## <a name="see-also"></a>Consulte también  
* [Tutorial: Agregar un gráfico circular a un informe (generador de informes)](Tutorial:%20Add%20a%20Pie%20Chart%20to%20Your%20Report%20\(Report%20Builder\).md)
*  [Gráficos circulares &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/pie-charts-report-builder-and-ssrs.md)   
*  [Aplicar formato a la leyenda de un gráfico &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/chart-legend-formatting-report-builder.md)   
*  [Mostrar las etiquetas de los puntos de datos fuera de un gráfico circular &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/display-data-point-labels-outside-a-pie-chart-report-builder-and-ssrs.md)   
 
  
