---
title: File_name (Transact-SQL) | Documentos de Microsoft
ms.custom: 
ms.date: 03/03/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- FILE_NAME_TSQL
- FILE_NAME
dev_langs:
- TSQL
helpviewer_keywords:
- viewing file names
- file names [SQL Server], FILE_NAME
- IDs [SQL Server], files
- file IDs [SQL Server]
- names [SQL Server], files
- displaying file names
- identification numbers [SQL Server], files
- FILE_NAME function
- logical file names [SQL Server]
ms.assetid: 68b298aa-ce47-4af5-b59f-9a1b46d48326
caps.latest.revision: 35
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: a2ca12bf5c6f5cfa3e9a7b44300119d5e55e57da
ms.contentlocale: es-es
ms.lasthandoff: 09/01/2017

---
# <a name="filename-transact-sql"></a>FILE_NAME (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx_md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  Devuelve el nombre de archivo lógico correspondiente a un número de identificación de archivo (Id.) dado.  
  
 ![Icono de vínculo de tema](../../database-engine/configure-windows/media/topic-link.gif "Icono de vínculo de tema") [Convenciones de sintaxis de Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
FILE_NAME ( file_id )   
```  
  
## <a name="arguments"></a>Argumentos  
 *file_ID*  
 Es el número de identificación del archivo cuyo nombre se va a devolver. *file_ID* es **int**.  
  
## <a name="return-types"></a>Tipos devueltos  
 **nvarchar (128)**  
  
## <a name="remarks"></a>Comentarios  
 *file_ID* corresponde a la columna file_id de las vistas de catálogo sys.master_files o sys.database_files.  
  
## <a name="examples"></a>Ejemplos  
 El ejemplo siguiente devuelve los nombres de archivo para `file`_`ID 1` y `file` \_ `ID` en el [!INCLUDE[ssSampleDBnormal](../../includes/sssampledbnormal-md.md)] base de datos.  
  
```tsql  
  
SELECT FILE_NAME(1) AS 'File Name 1', FILE_NAME(2) AS 'File Name 2';  
GO  
```  
  
 [!INCLUDE[ssResult](../../includes/ssresult-md.md)]  
  
 `File Name 1           File Name 2`  
  
 `----------------      ------------------------`  
  
 `AdventureWorks2012_Data   AdventureWorks2012_Log`  
  
 `(1 row(s) affected)`  
  
## <a name="see-also"></a>Vea también  
 [FILE_IDEX &#40; Transact-SQL &#41;](../../t-sql/functions/file-idex-transact-sql.md)   
 [Funciones de metadatos &#40; Transact-SQL &#41;](../../t-sql/functions/metadata-functions-transact-sql.md)   
 [sys.database_files &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-database-files-transact-sql.md)   
 [sys.master_files &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-master-files-transact-sql.md)  
  
  