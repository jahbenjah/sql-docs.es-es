---
title: referencia de depuración de clúster mssqlctl
titleSuffix: SQL Server big data clusters
description: Artículo de referencia para los comandos de clúster mssqlctl.
author: rothja
ms.author: jroth
manager: craigg
ms.date: 02/28/2019
ms.topic: reference
ms.prod: sql
ms.technology: big-data-cluster
ms.openlocfilehash: b12b0421cf32a36cfd6d681bc90ad9ca7c3f9209
ms.sourcegitcommit: 2de5446fbc57787f18a907dd5deb02a7831ec07d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2019
ms.locfileid: "58860556"
---
# <a name="mssqlctl-cluster-debug"></a>Depuración de clúster mssqlctl

[!INCLUDE[tsql-appliesto-ssver15-xxxx-xxxx-xxx](../includes/tsql-appliesto-ssver15-xxxx-xxxx-xxx.md)]

El siguiente artículo proporciona la referencia para la **depuración clúster** comandos en el **mssqlctl** herramienta. Para obtener más información acerca de otros **mssqlctl** comandos, consulte [mssqlctl referencia](reference-mssqlctl.md).

## <a id="commands"></a> Comandos

|||
|---|---|
| [copy-logs](#copy-logs) | Copiar los registros. |
| [volcado](#dump) | Volcado del registro de desencadenador. |

## <a id="copy-logs"></a> registros de copia de depuración del clúster

Copiar los registros.

```
mssqlctl cluster debug copy-logs
   --namespace
   [--container]
   [--pod]
   [--target-folder]
   [--timeout]
```

### <a name="parameters"></a>Parámetros

| Parámetros | Descripción |
|---|---|
| **--namespace -n** | Nombre del clúster, usado para el espacio de nombres de kubernetes. Requerido. |
| **--container -c** | Copiar los registros para los contenedores con un nombre similar, opcional, de forma predeterminada copia los registros para todos los contenedores. No se puede especificar varias veces. Si especifica varias veces, por última vez una se usará. |
| **--pod -p** | Copiar los registros para los pods con un nombre similar. Opcional, en los registros de copias de forma predeterminada para todos los pods. No se puede especificar varias veces. Si especifica varias veces, por última vez una se usará. |
| **---d de la carpeta de destino** | Ruta de acceso de carpeta de destino para copiar los registros a. Opcional, crea el resultado en la carpeta local de forma predeterminada.  No se puede especificar varias veces. Si especifica varias veces, por última vez una se usará. |
| **--timeout -t** | El número de segundos que deben transcurrir para que se complete el comando. El valor predeterminado es 0, lo que es ilimitado. |

## <a id="dump"></a> volcado de depuración de clúster

Volcado del registro de desencadenador.

```
mssqlctl cluster debug dump
   [--container]
   [--namespace]
   --target-folder
```

### <a name="parameters"></a>Parámetros

| Parámetros | Descripción |
|---|---|
| **--container -c** | Copiar los registros para los contenedores con un nombre similar, opcional, de forma predeterminada copia los registros para todos los contenedores. No se puede especificar varias veces. Si especifica varias veces, por última vez una se usará.  Los valores permitidos: mssql-controller. |
| **--namespace -n** | Nombre del clúster, usado para el espacio de nombres de kubernetes. Requerido. |
| **---d de la carpeta de destino** | Ruta de acceso de carpeta de destino para copiar los registros a. Opcional, crea el resultado en la carpeta local de forma predeterminada.  No se puede especificar varias veces. Si especifica varias veces, por última vez una se usará.  Valor predeterminado: `./output/dump`. Requerido. |

## <a name="next-steps"></a>Pasos siguientes

Para obtener más información acerca de otros **mssqlctl** comandos, consulte [mssqlctl referencia](reference-mssqlctl.md). Para obtener más información sobre cómo instalar el **mssqlctl** herramienta, consulte [instalar mssqlctl para administrar clústeres de SQL Server 2019 macrodatos](deploy-install-mssqlctl.md).