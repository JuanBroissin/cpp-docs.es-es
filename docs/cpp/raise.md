---
title: __raise
ms.date: 11/04/2016
f1_keywords:
- __raise
- __raise_cpp
helpviewer_keywords:
- __raise keyword [C++]
ms.assetid: 6f1ae418-5f0f-48b6-9f6e-8ea7e66b239a
ms.openlocfilehash: 865524fe91b7d137e3a943973dcca6d833bd16df
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50471443"
---
# <a name="raise"></a>__raise

Resalta el sitio de llamada de un evento.

## <a name="syntax"></a>Sintaxis

```
__raise method-declarator;
```

## <a name="remarks"></a>Comentarios

En código administrado, un evento solo se puede generar desde dentro de la clase donde se define. Consulte [evento](../windows/event-cpp-component-extensions.md) para obtener más información.

La palabra clave **__raise** genera un error que se genera si se llama a un no evento.

> [!NOTE]
>  Una clase o struct basada en plantilla no puede contener eventos.

## <a name="example"></a>Ejemplo

```cpp
// EventHandlingRef_raise.cpp
struct E {
   __event void func1();
   void func1(int) {}

   void func2() {}

   void b() {
      __raise func1();
      __raise func1(1);  // C3745: 'int Event::bar(int)':
                         // only an event can be 'raised'
      __raise func2();   // C3745
   }
};

int main() {
   E e;
   __raise e.func1();
   __raise e.func1(1);  // C3745
   __raise e.func2();   // C3745
}
```

## <a name="see-also"></a>Vea también

[Palabras clave](../cpp/keywords-cpp.md)<br/>
[Control de eventos](../cpp/event-handling.md)<br/>
[Extensiones de componentes para plataformas de tiempo de ejecución](../windows/component-extensions-for-runtime-platforms.md)