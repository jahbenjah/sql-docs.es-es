---
title: Credenciales de Oracle para ejecutar script | Microsoft Docs
ms.custom: ''
ms.date: 03/01/2017
ms.prod: sql
ms.prod_service: integration-services
ms.reviewer: ''
ms.technology: integration-services
ms.topic: conceptual
ms.assetid: 4a301cb0-2f5b-41ba-81bf-46b41d07f137
author: janinezhang
ms.author: janinez
manager: craigg
ms.openlocfilehash: a12faf8abe604adac73af56586b40338c5aa48cd
ms.sourcegitcommit: 7ccb8f28eafd79a1bddd523f71fe8b61c7634349
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2019
ms.locfileid: "58277494"
---
# <a name="oracle-credentials-for-running-script"></a>Credenciales de Oracle para ejecutar script
  Para ejecutar el script de registro complementario de Oracle desde la consola del Diseñador CDC de Oracle, el programa le solicitará las credenciales del usuario de Oracle que está ejecutando el script. Para ejecutar este script, el usuario de Oracle debe tener el permiso ALTER TABLE para todas las tablas que se van a capturar y el permiso SELECT en la vista DBA_LOG_GROUPS.  
  
## <a name="task-list"></a>Lista de tareas  
 Escriba lo siguiente en este cuadro de diálogo:  
  
 **Autenticación**  
  
 Seleccione una de las opciones siguientes:  
  
-   **Autenticación de Windows**: seleccione esta opción para usar las credenciales del dominio de Windows actual. Solo puede usar esta opción si la base de datos de Oracle está configurada para usar la autenticación de Windows.  
  
-   **Autenticación de Oracle**: si selecciona esta opción, debe escribir los valores de **Nombre de usuario** y **Contraseña** del usuario de la base de datos Oracle a la que se va a conectar.  
  
## <a name="see-also"></a>Consulte también  
 [Cómo administrar una instancia CDC](../../integration-services/change-data-capture/how-to-manage-a-cdc-instance.md)   
 [Revisar y generar Scripts de registro complementario](../../integration-services/change-data-capture/review-and-generate-supplemental-logging-scripts.md)  
  
  
