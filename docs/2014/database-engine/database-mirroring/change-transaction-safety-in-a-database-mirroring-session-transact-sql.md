---
title: Cambiar la seguridad de las transacciones en una sesión de creación de reflejo de la base de datos (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 06/13/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: high-availability
ms.topic: conceptual
helpviewer_keywords:
- transaction safety [SQL Server database mirroring]
ms.assetid: 8b03bb82-8589-4558-8545-9942fe008391
author: MikeRayMSFT
ms.author: mikeray
manager: craigg
ms.openlocfilehash: a79010a4fa59eaebfc743543799a1e83cc5e687d
ms.sourcegitcommit: 3da2edf82763852cff6772a1a282ace3034b4936
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/02/2018
ms.locfileid: "48133935"
---
# <a name="change-transaction-safety-in-a-database-mirroring-session-transact-sql"></a>Cambiar la seguridad de las transacciones en una sesión de creación de reflejo de la base de datos (Transact-SQL)
  La seguridad de las transacciones es el atributo que controla el modo operativo de la sesión. No obstante, el propietario de la base de datos puede cambiar la seguridad de las transacciones en cualquier momento. De forma predeterminada, el nivel de seguridad de las transacciones está establecido en FULL (modo operativo sincrónico).  
  
 Si se desactiva la seguridad de las transacciones, la sesión cambia al modo operativo asincrónico, lo que maximiza el rendimiento. Si la base de datos principal no está disponible, la base de datos reflejada se detiene pero está disponible como base de datos en espera semiactiva (la conmutación por error requiere forzar el servicio, con una posible pérdida de datos).  
  
### <a name="to-turn-on-transaction-safety"></a>Para activar la seguridad de las transacciones  
  
1.  Conéctese al servidor principal.  
  
2.  Escriba la instrucción Transact-SQL siguiente:  
  
    ```  
    ALTER DATABASE <database> SET PARTNER SAFETY FULL  
    ```  
  
     donde *\<base de datos>* es el nombre de la base de datos reflejada.  
  
### <a name="to-turn-off-transaction-safety"></a>Para desactivar la seguridad de las transacciones  
  
1.  Conéctese al servidor principal.  
  
2.  Emita la instrucción siguiente:  
  
    ```  
    ALTER DATABASE <database> SET PARTNER SAFETY OFF  
    ```  
  
     donde *\<base de datos>* es la base de datos reflejada.  
  
## <a name="see-also"></a>Vea también  
 [Reflejo de la base de datos ALTER DATABASE &#40;Transact-SQL&#41;](/sql/t-sql/statements/alter-database-transact-sql-database-mirroring)   
 [Database Mirroring Operating Modes](database-mirroring-operating-modes.md)  
  
  
