---
title: Error de las herramientas del vinculador LNK1123
ms.date: 12/29/2017
f1_keywords:
- LNK1123
helpviewer_keywords:
- LNK1123
ms.openlocfilehash: b67a2a4ddad13988967b7cc7d827862a2a6fe933
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50456425"
---
# <a name="linker-tools-error-lnk1123"></a>Error de las herramientas del vinculador LNK1123

> error durante la conversión a COFF: archivo no válido o dañado

Los archivos de entrada deben tener el formato de archivo de objeto común (COFF). Si un archivo de entrada no tiene el formato COFF, el vinculador intenta convertir automáticamente los objetos OMF de 32 bits a COFF o ejecuta CVTRES.EXE para convertir los archivos de recursos. Este mensaje indica que el vinculador no pudo convertir el archivo. También puede ocurrir al usar una versión incompatible de CVTRES.EXE desde otra instalación de Visual Studio, el kit de desarrollo de Windows o .NET Framework.

> [!NOTE]
> Si está ejecutando una versión anterior de Visual Studio, la conversión automática puede no ser compatible.

## <a name="to-fix-the-problem"></a>Para corregir el problema

- Aplique todos los service packs y actualizaciones para su versión de Visual Studio. Esto es especialmente importante para Visual Studio 2010.

- Intente compilar con la vinculación incremental deshabilitada. En la barra de menús, seleccione **Proyecto**, **Propiedades**. En el **páginas de propiedades** cuadro de diálogo, expanda **propiedades de configuración**, **vinculador**. Cambie el valor de **habilitar vinculación Incremental** a **No**.

- Compruebe que la versión de CVTRES.EXE que se encuentra primero en la variable de entorno PATH coincide con la versión de las herramientas de compilación, o la versión del conjunto de herramientas de la plataforma, utilizada por el proyecto.

- Pruebe a desactivar la opción Incrustar manifiesto. En la barra de menús, seleccione **Proyecto**, **Propiedades**. En el **páginas de propiedades** cuadro de diálogo, expanda **propiedades de configuración**, **herramienta manifiesto**, **de entrada y salida**. Cambie el valor de **incrustar manifiesto** a **No**.

- Asegúrese de que el tipo de archivo es válido. Por ejemplo, asegúrese de que un objeto OMF es de 32 bits y no de 16 bits. Para obtener más información, consulte [. Archivos obj como entrada del vinculador](../../build/reference/dot-obj-files-as-linker-input.md) y [formato PE](/windows/desktop/Debug/pe-format).

- Compruebe que el archivo no está dañado. Vuelva a compilar, si es necesario.

## <a name="see-also"></a>Vea también

[Archivos .obj como entrada del vinculador](../../build/reference/dot-obj-files-as-linker-input.md)<br/>
[Referencia de EDITBIN](../../build/reference/editbin-reference.md)<br/>
[Referencia de DUMPBIN](../../build/reference/dumpbin-reference.md)
