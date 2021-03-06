---
title: ¿Qué es el bloque de almacenamiento?
titleSuffix: SQL Server big data clusters
description: Este artículo describe el grupo de almacenamiento en un clúster de macrodatos de SQL Server 2019.
author: rothja
ms.author: jroth
manager: craigg
ms.date: 12/06/2018
ms.topic: conceptual
ms.prod: sql
ms.technology: big-data-cluster
ms.custom: seodec18
ms.openlocfilehash: b0775ac479b45dcb0fc0df23460b0fda0b783545
ms.sourcegitcommit: 2de5446fbc57787f18a907dd5deb02a7831ec07d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2019
ms.locfileid: "58860576"
---
# <a name="what-is-the-storage-pool-sql-server-big-data-clusters"></a>¿Qué es el bloque de almacenamiento (clústeres de macrodatos de SQL Server)?

[!INCLUDE[tsql-appliesto-ssver15-xxxx-xxxx-xxx](../includes/tsql-appliesto-ssver15-xxxx-xxxx-xxx.md)]

En este artículo se describe el rol de la *bloque de almacenamiento de SQL Server* en un clúster de macrodatos de 2019 de SQL Server (versión preliminar). Las secciones siguientes describen la arquitectura y la funcionalidad de un grupo de almacenamiento SQL.

## <a name="storage-pool-architecture"></a>Arquitectura del grupo de almacenamiento

El grupo de almacenamiento está formado por almacenamiento consta de los nodos de SQL Server en Linux, Spark y HDFS. Todos los nodos de almacenamiento en un clúster de macrodatos SQL son miembros de un clúster de HDFS.

![Arquitectura del grupo de almacenamiento](media/concept-storage-pool/scale-big-data-on-demand.png)

## <a name="responsibilities"></a>Responsabilidades

Son responsables de los nodos de almacenamiento:

- Ingesta de datos a través de Spark.
- Almacenamiento de datos en HDFS (formato Parquet). HDFS también proporciona persistencia de datos, como datos HDFS se reparten entre todos los nodos de almacenamiento del clúster de macrodatos SQL.
- Acceso a datos a través de extremos HDFS y SQL Server.

## <a name="next-steps"></a>Pasos siguientes

Para obtener más información acerca de los clústeres de macrodatos de SQL Server, consulte los siguientes recursos:

- [¿Qué son los clústeres de macrodatos de 2019 de SQL Server?](big-data-cluster-overview.md)
- [Taller: Arquitectura de clústeres de macrodatos de Microsoft SQL Server](https://github.com/Microsoft/sqlworkshops/tree/master/sqlserver2019bigdataclusters)
