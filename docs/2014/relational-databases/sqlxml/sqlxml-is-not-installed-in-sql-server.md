---
title: SQLXML no está instalado en SQL Server | Documentos de Microsoft
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql-server-2014
ms.reviewer: ''
ms.technology: ''
ms.topic: reference
ms.assetid: 3dbb4f65-41de-48b8-ad62-47c9d7932de3
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.openlocfilehash: 7561d2d22439112ea084f1f8a62c32aeb5591cfc
ms.sourcegitcommit: aa4f594ec6d3e85d0a1da6e69fa0c2070d42e1d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2019
ms.locfileid: "59240764"
---
# <a name="sqlxml-is-not-installed-in-sql-server"></a>SQLXML no se instala en SQL Server
  Antes de [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)], SQLXML 4.0 se comercializó junto con [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] y formó parte de la instalación predeterminada de todas las versiones de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)], salvo [!INCLUDE[ssExpress](../../includes/ssexpress-md.md)]. A partir de [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)], la última versión de SQLXML (SQLXML 4.0 SP1) ya no está incluida en [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]. Para instalar SQLXML 4.0 SP1 cuando esté disponible, descárguelo desde [ubicación de instalación para SQLXML SP1](https://www.microsoft.com/download/details.aspx?id=16978).  
  
 Si una aplicación se ejecuta en [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] y requiere SQLXML 4.0, y si el equipo no tiene instalado [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)], deberá descargar e instalar SQLXML 4.0 SP1.  
  
## <a name="sqlxml-40-sp1-behavior-with-new-data-types-using-sqloledb-and-sql-server-native-client-ole-db-provider"></a>Comportamiento de SQLXML 4.0 SP1 con nuevos tipos de datos que usan el proveedor OLE DB de SQLOLEDB y SQL Server Native Client  
 [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] presenta a los siguientes tipos de datos, es posible que desee utilizar que los desarrolladores de SQLXML:  
  
-   `Date`  
  
-   `Time`  
  
-   `DateTime2`  
  
-   `DateTimeOffset`  
  
 Cuando se usa SQLXML 4.0 SP1 con SQLOLEDB (de Data Access Components para Windows, anteriormente Microsoft Data Access Components) o el proveedor OLE DB de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] de [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)], estos nuevos tipos aparecerán como cadenas para el desarrollador. SQLXML 4.0 SP1 habilitará estos cuatro nuevos tipos de datos como tipos escalares integrados cuando se usan con el proveedor OLE DB de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Native Client11.0. Hasta que descargue SQLXML 4.0 SP1, la asignación de estos tipos a tipos que no sean de cadena puede producir el truncamiento de algunos datos. Por ejemplo, la asignación `DateTime2` a `xsd:date` hará que los datos se trunquen a la [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] `DateTime` precisión de 3,33 milisegundos.  
  
## <a name="see-also"></a>Vea también  
 [Conceptos de programación en SQLXML 4.0](sqlxml-4-0-programming-concepts.md)  
  
  
