---
title: OBJECTPROPERTY (Transact-SQL) | Documentos de Microsoft
ms.custom: 
ms.date: 03/15/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- OBJECTPROPERTY
- OBJECTPROPERTY_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- displaying schema-scoped object information
- viewing schema-scoped object information
- OBJECTPROPERTY function
- schema-scoped objects [SQL Server]
- objects [SQL Server], schema-scoped
ms.assetid: 27569888-f8b5-4cec-a79f-6ea6d692b4ae
caps.latest.revision: 81
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 0ee3350b200f0f42203a89d06ddb587b0792ee18
ms.contentlocale: es-es
ms.lasthandoff: 09/01/2017

---
# <a name="objectproperty-transact-sql"></a>OBJECTPROPERTY (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-all_md](../../includes/tsql-appliesto-ss2008-all-md.md)]

  Devuelve información acerca de los objetos de ámbito de esquema de la base de datos actual. Para obtener una lista de objetos con ámbito de esquema, consulte [sys.objects &#40; Transact-SQL &#41; ](../../relational-databases/system-catalog-views/sys-objects-transact-sql.md). Esta función no se puede utilizar para objetos que no pertenezcan al ámbito de esquema, como notificaciones de eventos y desencadenadores DDL (lenguaje de definición de datos).  
  
 ![Icono de vínculo de tema](../../database-engine/configure-windows/media/topic-link.gif "Icono de vínculo de tema") [Convenciones de sintaxis de Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Sintaxis  
  
```  
-- Syntax for SQL Server, Azure SQL Database, Azure SQL Data Warehouse, Parallel Data Warehouse  
  
OBJECTPROPERTY ( id , property )   
```  
  
## <a name="arguments"></a>Argumentos  
 *id*  
 Es una expresión que representa el identificador del objeto en la base de datos actual. *Id. de* es **int** y se supone que es un objeto de ámbito de esquema en el contexto de base de datos actual.  
  
 *propiedad*  
 Es una expresión que representa la información que se devuelve para el objeto especificado por *identificador*. *propiedad* puede ser uno de los siguientes valores.  
  
> [!NOTE]  
>  A menos que se indique lo contrario, se devuelve NULL si *propiedad* no es un nombre de propiedad válido, *identificador* no es un identificador de objeto válido, *identificador* es un tipo de objeto no compatible para el elemento especificado *propiedad*, o el autor de llamada no tiene permiso para ver los metadatos del objeto.  
  
|Nombre de la propiedad|Tipo de objeto|Descripción y valores devueltos|  
|-------------------|-----------------|-------------------------------------|  
|CnstIsClustKey|Restricción|Restricción PRIMARY KEY con un índice clúster.<br /><br /> 1 = True<br /><br /> 0 = False|  
|CnstIsColumn|Restricción|Restricción CHECK, DEFAULT o FOREIGN KEY en una única columna.<br /><br /> 1 = True<br /><br /> 0 = False|  
|CnstIsDeleteCascade|Restricción|Restricción FOREIGN KEY con la opción ON DELETE CASCADE.<br /><br /> 1 = True<br /><br /> 0 = False|  
|CnstIsDisabled|Restricción|Restricción deshabilitada.<br /><br /> 1 = True<br /><br /> 0 = False|  
|CnstIsNonclustKey|Restricción|Restricción PRIMARY KEY o UNIQUE con un índice no clúster.<br /><br /> 1 = True<br /><br /> 0 = False|  
|CnstIsNotRepl|Restricción|La restricción se define utilizando las palabras clave NOT FOR REPLICATION.<br /><br /> 1 = True<br /><br /> 0 = False|  
|CnstIsNotTrusted|Restricción|La restricción se ha habilitado sin comprobar las filas existentes, por lo que es posible que no se mantenga para todas las filas.<br /><br /> 1 = True<br /><br /> 0 = False|  
|CnstIsUpdateCascade|Restricción|Restricción FOREIGN KEY con la opción ON UPDATE CASCADE.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsAfterTrigger|Desencadenador|Desencadenador AFTER.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsAnsiNullsOn|Función de [!INCLUDE[tsql](../../includes/tsql-md.md)], procedimiento de [!INCLUDE[tsql](../../includes/tsql-md.md)], desencadenador de [!INCLUDE[tsql](../../includes/tsql-md.md)], vista|Valor de ANSI_NULLS en el momento de su creación.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsDeleteTrigger|Desencadenador|Desencadenador DELETE.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsFirstDeleteTrigger|Desencadenador|Primer desencadenador que se activa cuando se ejecuta DELETE en la tabla.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsFirstInsertTrigger|Desencadenador|Primer desencadenador que se activa cuando se ejecuta INSERT en la tabla.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsFirstUpdateTrigger|Desencadenador|Primer desencadenador que se activa cuando se ejecuta UPDATE en la tabla.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsInsertTrigger|Desencadenador|Desencadenador INSERT.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsInsteadOfTrigger|Desencadenador|Desencadenador INSTEAD OF.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsLastDeleteTrigger|Desencadenador|Último desencadenador que se activa cuando se ejecuta DELETE en la tabla.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsLastInsertTrigger|Desencadenador|Último desencadenador que se activa cuando se ejecuta INSERT en la tabla.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsLastUpdateTrigger|Desencadenador|Último desencadenador que se activa cuando se ejecuta UPDATE en la tabla.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsQuotedIdentOn|Función de [!INCLUDE[tsql](../../includes/tsql-md.md)], procedimiento de [!INCLUDE[tsql](../../includes/tsql-md.md)], desencadenador de [!INCLUDE[tsql](../../includes/tsql-md.md)], vista|Valor de QUOTED_IDENTIFIER en el momento de su creación.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsStartup|Procedimiento|Procedimiento de inicio.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsTriggerDisabled|Desencadenador|Desencadenador deshabilitado.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsTriggerNotForRepl|Desencadenador|Desencadenador definido como NOT FOR REPLICATION.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsUpdateTrigger|Desencadenador|Desencadenador UPDATE.<br /><br /> 1 = True<br /><br /> 0 = False|  
|ExecIsWithNativeCompilation|Procedimiento de [!INCLUDE[tsql](../../includes/tsql-md.md)]|**Se aplica a**: desde [!INCLUDE[ssSQL14](../../includes/sssql14-md.md)] hasta [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)].<br /><br /> El procedimiento se compila de forma nativa.<br /><br /> 1 = True<br /><br /> 0 = False<br /><br /> Tipo de datos base: **int**|  
|HasAfterTrigger|Tabla, vista|La tabla o la vista tiene un desencadenador AFTER.<br /><br /> 1 = True<br /><br /> 0 = False|  
|HasDeleteTrigger|Tabla, vista|La tabla o la vista tiene un desencadenador DELETE.<br /><br /> 1 = True<br /><br /> 0 = False|  
|HasInsertTrigger|Tabla, vista|La tabla o la vista tiene un desencadenador INSERT.<br /><br /> 1 = True<br /><br /> 0 = False|  
|HasInsteadOfTrigger|Tabla, vista|La tabla o la vista tiene un desencadenador INSTEAD OF.<br /><br /> 1 = True<br /><br /> 0 = False|  
|HasUpdateTrigger|Tabla, vista|La tabla o la vista tiene un desencadenador UPDATE.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsAnsiNullsOn|Función de [!INCLUDE[tsql](../../includes/tsql-md.md)], procedimiento de [!INCLUDE[tsql](../../includes/tsql-md.md)], tabla, desencadenador de [!INCLUDE[tsql](../../includes/tsql-md.md)], vista|Especifica que el valor de la opción ANSI NULLS de la tabla es ON. Esto significa que todas las comparaciones con un valor NULL se evalúan como UNKNOWN. Este valor se aplica a todas las expresiones de la definición de tabla, incluidas las columnas calculadas y las restricciones, mientras la tabla exista.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsCheckCnst|Cualquier objeto en el ámbito de esquema|Restricción CHECK.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsConstraint|Cualquier objeto en el ámbito de esquema|Es una restricción CHECK, DEFAULT o FOREIGN KEY de columna única en una columna o una tabla.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsDefault|Cualquier objeto en el ámbito de esquema|**Se aplica a**: desde [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] hasta [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)].<br /><br /> Valor predeterminado enlazado.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsDefaultCnst|Cualquier objeto en el ámbito de esquema|Restricción DEFAULT.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsDeterministic|Función, vista|Propiedad de determinismo de la función o vista.<br /><br /> 1 = Determinista<br /><br /> 0 = No determinista|  
|IsEncrypted|Función de [!INCLUDE[tsql](../../includes/tsql-md.md)], procedimiento de [!INCLUDE[tsql](../../includes/tsql-md.md)], tabla, desencadenador de [!INCLUDE[tsql](../../includes/tsql-md.md)], vista|Indica que el texto original de la instrucción del módulo se ha convertido a un formato confuso. La salida de la protección no es directamente visible en ninguna de las vistas de catálogo de [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)]. Los usuarios sin acceso a las tablas del sistema o archivos de base de datos no pueden recuperar el texto confuso. Sin embargo, el texto está disponible para los usuarios que pueden tener acceso a las tablas del sistema sobre el [puerto DAC](../../database-engine/configure-windows/diagnostic-connection-for-database-administrators.md) o directamente a los archivos de base de datos. Además, los usuarios que pueden adjuntar un depurador al proceso del servidor pueden recuperar el procedimiento original de la memoria en tiempo de ejecución.<br /><br /> 1 = Cifrada<br /><br /> 0 = No cifrado<br /><br /> Tipo de datos base: **int**|  
|IsExecuted|Cualquier objeto en el ámbito de esquema|El objeto se puede ejecutar (vista, procedimiento, función o desencadenador).<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsExtendedProc|Cualquier objeto en el ámbito de esquema|Procedimiento extendido.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsForeignKey|Cualquier objeto en el ámbito de esquema|Restricción FOREIGN KEY.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsIndexed|Tabla, vista|Tabla o vista que tiene un índice.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsIndexable|Tabla, vista|Tabla o vista en la que es posible crear un índice.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsInlineFunction|Función|Función insertada.<br /><br /> 1 = Función insertada<br /><br /> 0 = Función no insertada|  
|IsMSShipped|Cualquier objeto en el ámbito de esquema|Objeto creado durante la instalación de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)].<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsPrimaryKey|Cualquier objeto en el ámbito de esquema|Restricción PRIMARY KEY.<br /><br /> 1 = True<br /><br /> 0 = False<br /><br /> NULL = No es una función o el identificador de objeto no es válido.|  
|IsProcedure|Cualquier objeto en el ámbito de esquema|Procedimiento.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsQuotedIdentOn|Función de [!INCLUDE[tsql](../../includes/tsql-md.md)], procedimiento de [!INCLUDE[tsql](../../includes/tsql-md.md)], tabla, desencadenador de [!INCLUDE[tsql](../../includes/tsql-md.md)], vista, restricción CHECK, definición DEFAULT|Especifica que el valor del identificador entre comillas para el objeto es ON. Esto significa que los identificadores están delimitados por comillas dobles en todas las expresiones que participan en la definición del objeto.<br /><br /> 1 = ON <br /><br /> 0 = OFF|  
|IsQueue|Cualquier objeto en el ámbito de esquema|Cola de Service Broker<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsReplProc|Cualquier objeto en el ámbito de esquema|Procedimiento de replicación.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsRule|Cualquier objeto en el ámbito de esquema|Regla enlazada.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsScalarFunction|Función|Función con valores escalares.<br /><br /> 1 = Función escalar<br /><br /> 0 = Función no escalar|  
|IsSchemaBound|Función, vista|Función o vista enlazada al esquema creada mediante SCHEMABINDING.<br /><br /> 1 = Enlazada al esquema<br /><br /> 0 = No enlazada al esquema.|  
|IsSystemTable|Tabla|Tabla del sistema.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsTable|Tabla|Tabla.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsTableFunction|Función|Función con valores de tabla.<br /><br /> 1 = Función con valores de tabla<br /><br /> 0 = Función con valores no de tabla.|  
|IsTrigger|Cualquier objeto en el ámbito de esquema|Desencadenador.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsUniqueCnst|Cualquier objeto en el ámbito de esquema|Restricción UNIQUE.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsUserTable|Tabla|Tabla definida por el usuario.<br /><br /> 1 = True<br /><br /> 0 = False|  
|IsView|Ver|Vista.<br /><br /> 1 = True<br /><br /> 0 = False|  
|OwnerId|Cualquier objeto en el ámbito de esquema|Propietario del objeto.<br /><br /> **Nota:** el propietario del esquema no es necesariamente el propietario del objeto. Por ejemplo, los objetos secundarios (aquellos en los que *parent_object_id* es diferente de null) siempre devolverá el mismo identificador de propietario que el elemento primario.<br /><br /> Distinto de NULL = Identificador de usuario de base de datos que corresponde al propietario del objeto.|  
|TableDeleteTrigger|Tabla|La tabla tiene un desencadenador DELETE.<br /><br /> > 1 = identificador del primer desencadenador con el tipo especificado.|  
|TableDeleteTriggerCount|Tabla|La tabla tiene el número especificado de desencadenadores DELETE.<br /><br /> >0 = Número de desencadenadores DELETE.|  
|TableFullTextMergeStatus|Tabla|**Se aplica a**: desde [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] hasta [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)].<br /><br /> Indica si una tabla que tiene un índice de texto completo se está combinando actualmente.<br /><br /> 0 = La tabla no tiene un índice de texto completo o el índice de texto completo no se está combinando.<br /><br /> 1 = El índice de texto completo se está combinando.|  
|TableFullTextBackgroundUpdateIndexOn|Tabla|**Se aplica a**: desde [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] hasta [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)].<br /><br /> La tabla tiene habilitada la opción de actualización de índices de texto completo en segundo plano (seguimiento de cambios automáticos).<br /><br /> 1 = TRUE<br /><br /> 0 = False|  
|TableFulltextCatalogId|Tabla|**Se aplica a**: desde [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] hasta [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)].<br /><br /> Identificador del catálogo de texto completo en el que residen los datos de índice de texto completo para la tabla.<br /><br /> Distinto de cero = Identificador del catálogo de texto completo, asociado al índice único que identifica las filas en una tabla indizada de texto completo.<br /><br /> 0 = La tabla no tiene un índice de texto completo.|  
|TableFulltextChangeTrackingOn|Tabla|**Se aplica a**: desde [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] hasta [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)].<br /><br /> La tabla tiene habilitado el seguimiento de cambios de texto completo.<br /><br /> 1 = TRUE<br /><br /> 0 = False|  
|TableFulltextDocsProcessed|Tabla|**Se aplica a**: desde [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] hasta [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)].<br /><br /> Número de filas procesadas desde el comienzo de la indización de texto completo. En una tabla que se indiza para búsquedas en texto completo, todas las columnas de una fila se consideran como parte de un documento que se va a indizar.<br /><br /> 0 = No se ha completado ningún rastreo activo ni ninguna indización de texto completo.<br /><br /> > 0 = uno de los siguientes (A o B): A) el número de documentos procesados por insertar o actualizar operaciones desde el inicio de completo, Incremental o rellenado de seguimiento de cambios Manual. B) el número de filas procesadas por insert o las operaciones de actualización desde que se habilitó el seguimiento de cambios con rellenado del índice de actualización de fondo, el esquema de índice de texto completo cambia, la regeneración del catálogo de texto completo o la instancia de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] reinicien y así sucesivamente.<br /><br /> NULL = La tabla no tiene un índice de texto completo.<br /><br /> Esta propiedad no supervisa ni cuenta las filas eliminadas.|  
|TableFulltextFailCount|Tabla|**Se aplica a**: desde [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] hasta [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)].<br /><br /> Número de filas no indizadas por Búsqueda de texto completo.<br /><br /> 0 = El rellenado se ha completado.<br /><br /> > 0 = uno de los siguientes (A o B): A) el número de documentos no indizados desde el inicio del llenado de seguimiento de cambios completo, Incremental o actualización Manual. B) para seguimiento de cambios con fondo actualización de índices, el número de filas que no indizados desde el principio de la población o el reinicio de la población. Esto puede deberse a un cambio del esquema, a la regeneración del catálogo, al reinicio del servidor, etc.<br /><br /> NULL = La tabla no tiene un índice de texto completo.|  
|TableFulltextItemCount|Tabla|**Se aplica a**: desde [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] hasta [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)].<br /><br /> Número de filas para las que se crearon índices de texto completo correctamente.|  
|TableFulltextKeyColumn|Tabla|**Se aplica a**: desde [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] hasta [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)].<br /><br /> Identificador de la columna asociada al índice de columna único que participa en la definición de índice de texto completo.<br /><br /> 0 = La tabla no tiene un índice de texto completo.|  
|TableFulltextPendingChanges|Tabla|**Se aplica a**: desde [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] hasta [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)].<br /><br /> Número de entradas de seguimiento de cambios pendientes de procesamiento.<br /><br /> 0 = El seguimiento de cambios no está habilitado.<br /><br /> NULL = La tabla no tiene un índice de texto completo.|  
|TableFulltextPopulateStatus|Tabla|**Se aplica a**: desde [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] hasta [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)].<br /><br /> 0 = Inactiva<br /><br /> 1 = Rellenado completo en curso.<br /><br /> 2 = Rellenado incremental en curso.<br /><br /> 3 = Propagación de cambios de seguimiento en curso.<br /><br /> 4 = el índice de actualización está en curso, como el seguimiento de cambios automáticos de fondo.<br /><br /> 5 = Indización de texto completo acelerada o pausada.|  
|TableHasActiveFulltextIndex|Tabla|**Se aplica a**: desde [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] hasta [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)].<br /><br /> La tabla tiene un índice de texto completo activo.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasCheckCnst|Tabla|La tabla tiene una restricción CHECK.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasClustIndex|Tabla|La tabla tiene un índice clúster.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasDefaultCnst|Tabla|La tabla tiene una restricción DEFAULT.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasDeleteTrigger|Tabla|La tabla tiene un desencadenador DELETE.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasForeignKey|Tabla|La tabla tiene una restricción FOREIGN KEY.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasForeignRef|Tabla|Una restricción FOREIGN KEY hace referencia a la tabla.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasIdentity|Tabla|La tabla tiene una columna de identidad.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasIndex|Tabla|La tabla tiene un índice de cualquier tipo.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasInsertTrigger|Tabla|El objeto tiene un desencadenador INSERT.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasNonclustIndex|Tabla|La tabla tiene un índice no clúster.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasPrimaryKey|Tabla|La tabla tiene una clave principal.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasRowGuidCol|Tabla|La tabla tiene un ROWGUIDCOL para una **uniqueidentifier** columna.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasTextImage|Tabla|La tabla tiene un **texto**, **ntext**, o **imagen** columna.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasTimestamp|Tabla|La tabla tiene un **timestamp** columna.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasUniqueCnst|Tabla|La tabla tiene una restricción UNIQUE.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasUpdateTrigger|Tabla|Objeto tiene un desencadenador UPDATE.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableHasVarDecimalStorageFormat|Tabla|Tabla está habilitada para **vardecimal** el formato de almacenamiento.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableInsertTrigger|Tabla|La tabla tiene un desencadenador INSERT.<br /><br /> > 1 = identificador del primer desencadenador con el tipo especificado.|  
|TableInsertTriggerCount|Tabla|Tabla tiene el número especificado de desencadenadores INSERT.<br /><br /> >0 = Número de desencadenadores INSERT.|  
|TableIsFake|Tabla|La tabla no es real. [!INCLUDE[ssDEnoversion](../../includes/ssdenoversion-md.md)] la materializa internamente a petición.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableIsLockedOnBulkLoad|Tabla|Tabla está bloqueada debido a un **bcp** o BULK INSERT.<br /><br /> 1 = True<br /><br /> 0 = False|  
|TableIsMemoryOptimized|Tabla|**Se aplica a**: desde [!INCLUDE[ssSQL14](../../includes/sssql14-md.md)] hasta [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)].<br /><br /> La tabla tiene optimización para memoria<br /><br /> 1 = True<br /><br /> 0 = False<br /><br /> Tipo de datos base: **int**<br /><br /> Para obtener más información, vea [OLTP en memoria &#40;optimización en memoria&#41;](../../relational-databases/in-memory-oltp/in-memory-oltp-in-memory-optimization.md).|  
|TableIsPinned|Tabla|La tabla se ancla para que se mantenga en la memoria caché de datos.<br /><br /> 0 = False<br /><br /> Esta característica no se admite en [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] ni en versiones posteriores.|  
|TableTextInRowLimit|Tabla|Número máximo de bytes permitidos para text in row.<br /><br /> 0 si no se ha establecido la opción text in row.|  
|TableUpdateTrigger|Tabla|La tabla tiene un desencadenador UPDATE.<br /><br /> > 1 = Identificador del primer desencadenador con el tipo especificado.|  
|TableUpdateTriggerCount|Tabla|La tabla tiene el número especificado de desencadenadores UPDATE.<br /><br /> > 0 = Número de desencadenadores UPDATE.|  
|TableHasColumnSet|Tabla|La tabla tiene un conjunto de columnas.<br /><br /> 0 = False<br /><br /> 1 = True<br /><br /> Para obtener más información, vea [Usar conjuntos de columnas](../../relational-databases/tables/use-column-sets.md).|  
|TableTemporalType|Tabla|**Se aplica a**: desde [!INCLUDE[ssSQL15](../../includes/sssql15-md.md)] hasta [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)].<br /><br /> Especifica el tipo de tabla.<br /><br /> 0 = la tabla no temporal<br /><br /> 1 = la tabla de historial para la tabla con control de versiones<br /><br /> 2 = tabla temporal con versión del sistema|  
  
## <a name="return-types"></a>Tipos devueltos  
 **int**  
  
## <a name="exceptions"></a>Excepciones  
 Devuelve NULL si se produce un error o si el autor de la llamada no tiene permiso para ver el objeto.  
  
 Un usuario solo puede ver los metadatos de elementos protegibles que posea o para los que se le haya concedido permiso. Esto significa que las funciones integradas de emisión de metadatos, como OBJECTPROPERTY, pueden devolver NULL si el usuario no tiene ningún permiso para el objeto. Para obtener más información, consulte [Metadata Visibility Configuration](../../relational-databases/security/metadata-visibility-configuration.md).  
  
## <a name="remarks"></a>Comentarios  
 El [!INCLUDE[ssDE](../../includes/ssde-md.md)] se da por supuesto que *object_id* está en el contexto de base de datos actual. Una consulta que hace referencia a un *object_id* en otra base de datos devolverá NULL o resultados incorrectos. Por ejemplo, en la siguiente consulta el contexto de base de datos actual es la base de datos maestra. El [!INCLUDE[ssDE](../../includes/ssde-md.md)] intentará devolver el valor de propiedad para el elemento especificado *object_id* en esa base de datos en lugar de la base de datos especificado en la consulta. La consulta devuelve resultados incorrectos porque la vista `vEmployee` no está en la base de datos maestra.  
  
```  
USE master;  
GO  
SELECT OBJECTPROPERTY(OBJECT_ID(N'AdventureWorks2012.HumanResources.vEmployee'), 'IsView');  
GO  
```  
  
 OBJECTPROPERTY (*view_id*, 'IsIndexable') puede consumir importantes recursos del equipo porque la evaluación de la propiedad IsIndexable requiere el análisis de la definición de la vista, la normalización y optimización parcial. Aunque la propiedad IsIndexable identifica tablas o vistas que se pueden indizar, es posible que se produzca un error en la creación real del índice si no se cumplen ciertos requisitos de clave de índice. Para obtener más información, vea [CREATE INDEX &#40;Transact-SQL&#41;](../../t-sql/statements/create-index-transact-sql.md).  
  
 OBJECTPROPERTY (*table_id*, 'TableHasActiveFulltextIndex') devolverá un valor de 1 (true) cuando se agrega al menos una columna de una tabla para la indización. El índice de texto completo se activa para su llenado en el momento en que se agrega la primera columna para la indización.  
  
 Al crear una tabla, la opción QUOTED IDENTIFIER siempre se almacena como ON en los metadatos de la tabla, incluso si la opción está establecida en OFF al crear la tabla. Por lo tanto, OBJECTPROPERTY (*table_id*, 'IsQuotedIdentOn') siempre devolverá un valor de 1 (true).  
  
## <a name="examples"></a>Ejemplos  
  
### <a name="a-verifying-that-an-object-is-a-table"></a>A. Comprobar si un objeto es una tabla  
 En el ejemplo siguiente se comprueba si `UnitMeasure` es una tabla de la base de datos [!INCLUDE[ssSampleDBobject](../../includes/sssampledbobject-md.md)].  
  
```  
USE AdventureWorks2012;  
GO  
IF OBJECTPROPERTY (OBJECT_ID(N'Production.UnitMeasure'),'ISTABLE') = 1  
   PRINT 'UnitMeasure is a table.'  
ELSE IF OBJECTPROPERTY (OBJECT_ID(N'Production.UnitMeasure'),'ISTABLE') = 0  
   PRINT 'UnitMeasure is not a table.'  
ELSE IF OBJECTPROPERTY (OBJECT_ID(N'Production.UnitMeasure'),'ISTABLE') IS NULL  
   PRINT 'ERROR: UnitMeasure is not a valid object.';  
GO  
  
```  
  
### <a name="b-verifying-that-a-scalar-valued-user-defined-function-is-deterministic"></a>B. Comprobar si una función escalar definida por el usuario es determinista  
 El ejemplo siguiente se comprueba si la función escalar definida por el usuario `ufnGetProductDealerPrice`, que devuelve un **dinero** valor, es determinista.  
  
```  
USE AdventureWorks2012;  
GO  
SELECT OBJECTPROPERTY(OBJECT_ID('dbo.ufnGetProductDealerPrice'), 'IsDeterministic');  
GO  
```  
  
 El conjunto de resultados muestra que `ufnGetProductDealerPrice` no es una función determinista.  
  
 `-----`  
  
 `0`  
  
### <a name="c-finding-the-objects-that-belong-to-a-specific-schema"></a>C. Buscar los objetos que pertenecen a un esquema específico  
 En el siguiente ejemplo se utiliza la propiedad `SchemaId` para devolver todos los objetos que pertenecen al esquema `Production`.  
  
```  
USE AdventureWorks2012;  
GO  
SELECT name, object_id, type_desc  
FROM sys.objects   
WHERE OBJECTPROPERTY(object_id, N'SchemaId') = SCHEMA_ID(N'Production')  
ORDER BY type_desc, name;  
GO  
```  
  
## <a name="examples-includesssdwfullincludessssdwfull-mdmd-and-includesspdwincludessspdw-mdmd"></a>Ejemplos: [!INCLUDE[ssSDWfull](../../includes/sssdwfull-md.md)] y[!INCLUDE[ssPDW](../../includes/sspdw-md.md)]  
  
### <a name="d-verifying-that-an-object-is-a-table"></a>Comprobar que un objeto es una tabla D:  
 En el ejemplo siguiente se comprueba si `dbo.DimReseller` es una tabla de la base de datos [!INCLUDE[ssawPDW](../../includes/ssawpdw-md.md)].  
  
```  
-- Uses AdventureWorks  
  
IF OBJECTPROPERTY (OBJECT_ID(N'dbo.DimReseller'),'ISTABLE') = 1  
   SELECT 'DimReseller is a table.'  
ELSE   
   SELECT 'DimReseller is not a table.';  
GO  
```  
  
### <a name="e-finding-the-tables-that-belong-to-a-specific-schema"></a>E: buscar las tablas que pertenecen a un esquema específico  
 El ejemplo siguiente devuelve todas las tablas en el esquema dbo.  
  
```  
-- Uses AdventureWorks  
  
SELECT name, object_id, type_desc  
FROM sys.objects   
WHERE OBJECTPROPERTY(object_id, N'SchemaId') = SCHEMA_ID(N'dbo')  
ORDER BY type_desc, name;  
GO  
```  
  
## <a name="see-also"></a>Vea también  
 [COLUMNPROPERTY &#40; Transact-SQL &#41;](../../t-sql/functions/columnproperty-transact-sql.md)   
 [Funciones de metadatos &#40; Transact-SQL &#41;](../../t-sql/functions/metadata-functions-transact-sql.md)   
 [OBJECTPROPERTYEX &#40; Transact-SQL &#41;](../../t-sql/functions/objectpropertyex-transact-sql.md)   
 [ALTER AUTHORIZATION &#40; Transact-SQL &#41;](../../t-sql/statements/alter-authorization-transact-sql.md)   
 [TYPEPROPERTY &#40; Transact-SQL &#41;](../../t-sql/functions/typeproperty-transact-sql.md)   
 [Sys.Objects &#40; Transact-SQL &#41;](../../relational-databases/system-catalog-views/sys-objects-transact-sql.md)  
  
  

