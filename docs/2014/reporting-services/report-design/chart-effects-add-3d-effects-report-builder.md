---
title: Agregar efectos 3D a un gráfico (Generador de informes y SSRS) | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.suite: ''
ms.technology:
- reporting-services-native
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: ab9625d8-6557-4a4d-8123-eefa7c066ff5
caps.latest.revision: 5
author: douglaslM
ms.author: douglasl
manager: mblythe
ms.openlocfilehash: 99a350febe4166293664e51a17978e66d7d25f97
ms.sourcegitcommit: 5dd5cad0c1bbd308471d6c885f516948ad67dfcf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2018
ms.locfileid: "36204095"
---
# <a name="add-3d-effects-to-a-chart-report-builder-and-ssrs"></a>Agregar efectos 3D a un gráfico (Generador de informes y SSRS)
  Se pueden usar efectos tridimensionales (3D) para dar profundidad y agregar impacto visual a un gráfico. Por ejemplo, si desea resaltar un sector específico de un gráfico circular seccionado, puede girar y cambiar la perspectiva del gráfico para que los usuarios se fijen primero en dicho sector. Cuando se aplican efectos 3D al gráfico, se deshabilitan todos los colores de degradado y los estilos de sombreado.  
  
> [!NOTE]  
>  [!INCLUDE[ssRBRDDup](../../includes/ssrbrddup-md.md)]  
  
### <a name="to-apply-3d-effects-to-a-range-area-line-scatter-or-polar-chart"></a>Para aplicar efectos 3D a un gráfico de intervalos, áreas, líneas, dispersión o polar  
  
1.  Haga clic con el botón derecho en cualquier parte dentro del área del gráfico y seleccione **Efectos 3D**. Aparecerá el cuadro de diálogo **Propiedades del área de gráfico** .  
  
2.  En **Opciones 3D**, seleccione la opción **Habilitar 3D** .  
  
3.  (Opcional) En **Opciones 3D**, puede establecer diversas propiedades relacionadas con opciones de ángulos y escenas 3D. Para obtener más información acerca de estas propiedades, vea [3D, bisel y otros efectos a un gráfico &#40;el generador de informes y SSRS&#41;](chart-effects-3d-bevel-and-other-report-builder.md).  
  
4.  Haga clic en **Aceptar**.  
  
### <a name="to-apply-3d-effects-to-a-funnel-chart"></a>Para aplicar efectos 3D a un gráfico de embudo  
  
1.  Haga clic con el botón derecho en cualquier parte dentro del área del gráfico y seleccione **Efectos 3D**. Aparecerá el cuadro de diálogo **Propiedades del área de gráfico** .  
  
2.  En **Opciones 3D**, seleccione la opción **Habilitar 3D** . Haga clic en **Aceptar**.  
  
3.  (Opcional) Para personalizar el aspecto visual del gráfico de embudo, puede ir al panel Propiedades y cambiar propiedades específicas para ese tipo de gráfico.  
  
    1.  Abra el panel de propiedades.  
  
    2.  En la superficie de diseño, haga clic en cualquier parte del gráfico de embudo. Se muestran las propiedades de las series del gráfico de embudo en el panel de propiedades.  
  
    3.  En la sección **General** , expanda el nodo **CustomAttributes** .  
  
    4.  Para la propiedad **Funnel3DDrawingStyle** , seleccione si el embudo se mostrará como circular o cuadrado.  
  
    5.  Para la propiedad **Funnel3DRotationAngle** , establezca un valor entre -10 y 10. Esto determinará el grado de inclinación que se mostrará en el gráfico de embudo 3D.  
  
### <a name="to-apply-3d-effects-to-a-pie-chart"></a>Para aplicar efectos 3D a un gráfico circular  
  
1.  Haga clic con el botón secundario en cualquier parte dentro del área del gráfico y seleccione Efectos 3D. Aparecerá el cuadro de diálogo **Propiedades del área de gráfico** .  
  
2.  En **Opciones 3D**, seleccione la opción **Habilitar 3D** . Haga clic en **Aceptar**.  
  
3.  (Opcional) En **Giro**, escriba un valor entero que represente el giro horizontal del gráfico circular.  
  
4.  (Opcional) En **Inclinación**, escriba un valor entero que represente el giro de inclinación vertical del gráfico circular.  
  
5.  Haga clic en **Aceptar**.  
  
### <a name="to-apply-3d-effects-to-a-bar-or-column-chart"></a>Para aplicar efectos 3D a un gráfico de barras o de columnas  
  
1.  Haga clic con el botón derecho en cualquier parte dentro del área del gráfico y seleccione **Efectos 3D**. Aparecerá el cuadro de diálogo **Propiedades del área de gráfico** .  
  
2.  Seleccione la opción **Habilitar 3D** . Haga clic en **Aceptar**.  
  
3.  (Opcional) Seleccione la opción **Habilitar agrupación en clústeres** . Si el gráfico contiene varias series de gráficos de barras o de columnas, esta opción mostrará las series agrupadas en clústeres. De forma predeterminada, cuando hay varias series de barras o de columnas se muestran unas al lado de otras.  
  
4.  Haga clic en **Aceptar**.  
  
5.  (Opcional) Para agregar efectos de cilindro a un gráfico de barras o de columnas, siga estos pasos:  
  
    1.  Abra el panel de propiedades.  
  
    2.  En la superficie de diseño, haga clic en cualquiera de las barras en la serie. Las propiedades de la serie se muestran en el panel de propiedades.  
  
    3.  En la sección **General** , expanda el nodo **CustomAttributes** .  
  
    4.  Para la propiedad **DrawingStyle** , especifique el valor **Cylinder** .  
  
## <a name="see-also"></a>Vea también  
 [3D, bisel y otros efectos a un gráfico de &#40;el generador de informes SSRS&#41;](chart-effects-3d-bevel-and-other-report-builder.md)   
 [Aplicar formato a un gráfico &#40;Generador de informes y SSRS&#41;](formatting-a-chart-report-builder-and-ssrs.md)   
 [Gráficos &#40;el generador de informes SSRS&#41;](charts-report-builder-and-ssrs.md)  
  
  