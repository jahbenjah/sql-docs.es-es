---
title: CEILING (expresión de SSIS) | Microsoft Docs
ms.custom: ''
ms.date: 03/01/2017
ms.prod: sql
ms.prod_service: integration-services
ms.reviewer: ''
ms.technology: integration-services
ms.topic: conceptual
helpviewer_keywords:
- smallest integer great than or equal to expression
- CEILING function [SSIS]
ms.assetid: c35bd4ee-1ab6-46ab-89a7-cf771527faa2
author: janinezhang
ms.author: janinez
manager: craigg
ms.openlocfilehash: c69ce4ea1890048af41ccd081ea9d2204a6ac637
ms.sourcegitcommit: 7ccb8f28eafd79a1bddd523f71fe8b61c7634349
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2019
ms.locfileid: "58275110"
---
# <a name="ceiling-ssis-expression"></a>CEILING (expresión de SSIS)
  Devuelve el menor entero mayor o igual que una expresión numérica.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
CEILING(numeric_expression)  
```  
  
## <a name="arguments"></a>Argumentos  
 *numeric_expression*  
 Expresión numérica válida.  
  
## <a name="result-types"></a>Tipos de resultado  
 El tipo de datos de la expresión numérica pasada a la función.  
  
## <a name="remarks"></a>Notas  
 CEILING devuelve un resultado NULL si el valor del argumento es NULL.  
  
## <a name="expression-examples"></a>Ejemplos de expresiones  
 Estos ejemplos aplican la función CEILING a valores positivos, negativos y cero.  
  
```  
CEILING(123.74)  
```  
  
 Devuelve 124.00.  
  
```  
CEILING(-124.27)  
```  
  
 Devuelve -124.00.  
  
```  
CEILING(0.00)  
```  
  
 Devuelve 0,00.  
  
## <a name="see-also"></a>Consulte también  
 [FLOOR &#40;expresión de SSIS&#41;](../../integration-services/expressions/floor-ssis-expression.md)   
 [Funciones &#40;expresión de SSIS&#41;](../../integration-services/expressions/functions-ssis-expression.md)  
  
  
