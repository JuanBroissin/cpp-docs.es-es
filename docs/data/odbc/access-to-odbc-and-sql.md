---
title: Acceso a ODBC y SQL
ms.date: 11/04/2016
helpviewer_keywords:
- API calls [C++], calling DAO or ODBC directly
- Windows API [C++], calling from MFC
- ODBC API functions [C++]
- ODBC API functions [C++], calling from MFC
- SQL [C++], calling ODBC API functions
- ODBC [C++], API functions
ms.assetid: 5613d7dc-00b7-4646-99ae-1116c05c52b4
ms.openlocfilehash: 97aa0f6318a47a93b0079a81dea772b900b5484b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50441774"
---
# <a name="access-to-odbc-and-sql"></a>Acceso a ODBC y SQL

La biblioteca Microsoft Foundation Class encapsula muchas llamadas de API de Windows y todavía le permite llamar directamente a cualquier función de la API de Windows. Las clases de base de datos proporcionan la misma flexibilidad con respecto a la API de ODBC. Mientras que las clases de base de datos de gran parte de la complejidad de ODBC blindar, puede llamar a funciones API de ODBC directamente desde cualquier lugar en el programa.

De forma similar, las clases de base de datos evitan tener que trabajar mucho con [SQL](../../data/odbc/sql.md), pero se puede usar SQL directamente si desea. Puede personalizar los objetos de conjunto de registros pasando una instrucción SQL personalizada (o partes de la configuración de la instrucción predeterminada) al abrir el conjunto de registros. También puede realizar llamadas a SQL directamente mediante el [ExecuteSQL](../../mfc/reference/cdatabase-class.md#executesql) función miembro de clase [CDatabase](../../mfc/reference/cdatabase-class.md).

Para obtener más información, consulte [ODBC: llamar a ODBC API directamente a funciones](../../data/odbc/odbc-calling-odbc-api-functions-directly.md) y [SQL: realizar directo SQL llamadas (ODBC)](../../data/odbc/sql-making-direct-sql-calls-odbc.md).

## <a name="see-also"></a>Vea también

[ODBC y MFC](../../data/odbc/odbc-and-mfc.md)