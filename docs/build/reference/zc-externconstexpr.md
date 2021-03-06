---
title: '/ Zc: externconstexpr (habilitar las variables del extern constexpr)'
ms.date: 02/28/2018
f1_keywords:
- /Zc:externConstexpr
helpviewer_keywords:
- -Zc:externConstexpr compiler option (C++)
- extern constexpr variables (C++)
ms.assetid: 4da5e33a-2e4d-4ed2-8616-bd8f43265c27
ms.openlocfilehash: a9efa2fa191cbdda99e057ac9329d79bc598743c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50510700"
---
# <a name="zcexternconstexpr-enable-extern-constexpr-variables"></a>/ Zc: externconstexpr (habilitar las variables del extern constexpr)

El **/Zc: externconstexpr** opción del compilador indica al compilador que se ajusta al estándar de C++ y permiten una vinculación externa para `constexpr` variables. De forma predeterminada, Visual Studio siempre da un `constexpr` vinculación interna de variable, incluso si se especifica la `extern` palabra clave.

## <a name="syntax"></a>Sintaxis

> **/ Zc: externconstexpr**[**-**]

## <a name="remarks"></a>Comentarios

El **/Zc: externconstexpr** opción del compilador hace que el compilador vinculación externa se aplican a las variables declaradas con `extern constexpr`. En versiones anteriores de Visual Studio y de forma predeterminada o si **/Zc:externConstexpr-** se especifica, Visual Studio aplica vinculación interna a `constexpr` aunque se utilicen las variables el `extern` se utiliza la palabra clave. El **/Zc: externconstexpr** opción está disponible a partir de Visual Studio 2017 15.6 de actualización. y está desactivada de forma predeterminada. El [/ permissive-](permissive-standards-conformance.md) no habilita la opción **/Zc: externconstexpr**.

Si un archivo de encabezado contiene una variable declarada `extern constexpr`, debe marcarse [__declspec (selectany)](../../cpp/selectany.md) para combinar las declaraciones duplicadas en una sola instancia en el archivo binario vinculado. En caso contrario, es posible que vea errores del vinculador, por ejemplo, LNK2005, las infracciones de la regla de definición de.

### <a name="to-set-this-compiler-option-in-visual-studio"></a>Para establecer esta opción del compilador en Visual Studio

1. Abra el cuadro de diálogo **Páginas de propiedades** del proyecto. Para obtener más información, vea [Trabajar con propiedades del proyecto](../../ide/working-with-project-properties.md).

1. Seleccione el **propiedades de configuración** > **C o C++** > **línea de comandos** página de propiedades.

1. Agregar **/Zc: externconstexpr** o **/Zc:externConstexpr-** a la **opciones adicionales:** panel.

## <a name="see-also"></a>Vea también

[/Zc (Ajuste)](../../build/reference/zc-conformance.md)<br/>
[Auto (palabra clave)](../../cpp/auto-keyword.md)