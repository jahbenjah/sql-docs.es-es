---
title: Destino de conjunto de registros | Microsoft Docs
ms.custom: ''
ms.date: 03/01/2017
ms.prod: sql
ms.prod_service: integration-services
ms.reviewer: ''
ms.technology: integration-services
ms.topic: conceptual
f1_keywords:
- sql13.dts.designer.recordsetdest.f1
helpviewer_keywords:
- Recordset destination
- ADO recordsets [Integration Services]
- destinations [Integration Services], Recordset
- in-memory ADO recordsets [Integration Services]
ms.assetid: be973cf1-c4ff-49f8-987e-314c08ef98e4
author: janinezhang
ms.author: janinez
manager: craigg
ms.openlocfilehash: c8f12ca10a98e278d43023bebcb1c3b3d6b169d8
ms.sourcegitcommit: 7ccb8f28eafd79a1bddd523f71fe8b61c7634349
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2019
ms.locfileid: "58281649"
---
# <a name="recordset-destination"></a>destino de conjunto de registros
  El destino de conjunto de registros crea y llena un conjunto de registros ADO almacenado en la memoria. La forma del conjunto de registros se define según la entrada al destino de conjunto de registros en el tiempo de diseño.  
  
## <a name="configuration-of-the-recordset-destination"></a>Configuración del destino de conjunto de registros  
 El destino de conjunto de registros se configura especificando la variable que almacena el conjunto de registros ADO.  
  
 En tiempo de ejecución, el conjunto de registros ADO se escribe en la variable de tipo Object especificada en la propiedad VariableName del destino de conjunto de registros. A continuación, la variable pone el conjunto de registros a disposición fuera del flujo de datos, donde lo pueden usar scripts y otros elementos del paquete.  
  
 Este origen tiene una entrada. No admite una salida de error.  
  
 Puede establecer propiedades a través del Diseñador de [!INCLUDE[ssIS](../../includes/ssis-md.md)] o mediante programación.  
  
 El cuadro de diálogo **Editor avanzado** indica las propiedades que se pueden establecer mediante programación. Para obtener más información acerca de las propiedades que puede establecer a través del cuadro de diálogo **Editor avanzado** o mediante programación, haga clic en uno de los temas siguientes:  
  
-   [Propiedades comunes](https://msdn.microsoft.com/library/51973502-5cc6-4125-9fce-e60fa1b7b796)  
  
-   [Propiedades personalizadas del destino de conjunto de registros](../../integration-services/data-flow/recordset-destination-custom-properties.md)  
  
 Para más información sobre cómo establecer las propiedades, vea [Establecer las propiedades de un componente de flujo de datos](../../integration-services/data-flow/set-the-properties-of-a-data-flow-component.md).  
  
## <a name="related-tasks"></a>Related Tasks  
 [Usar un destino de conjunto de registros](../../integration-services/data-flow/use-a-recordset-destination.md)  
  
  
