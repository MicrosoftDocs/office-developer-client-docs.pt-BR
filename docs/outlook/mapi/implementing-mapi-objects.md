---
title: Implementando objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c0d67d10d54591de926724cbf594a44f17e9ea14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310168"
---
# <a name="implementing-mapi-objects"></a>Implementando objetos MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os objetos MAPI podem ser implementados usando classes C++ ou estruturas de dados C, dependendo da linguagem e do conjunto de APIs que um cliente ou provedor de serviços está usando. Os provedores de serviços podem ser escritos em C ou C++ com a interface do provedor de serviços MAPI; os aplicativos cliente também podem usar C ou C++. Se possível, os clientes e provedores de serviços que usam a interface de programação orientada a objeto devem usar C++. 
  
O C++ é a opção preferida porque o MAPI é uma tecnologia orientada a objetos, e o C++ se permite mais prontamente para o desenvolvimento orientado a objetos. O código resultante é mais simples e mais simples, facilitando a manutenção. A documentação de MAPI é escrita principalmente para desenvolvedores C++; todas as descrições de sintaxe para os métodos de interface MAPI nesta referência estão em C++.
  
Os desenvolvedores podem usar o Microsoft Visual Studio e ferramentas de desenvolvimento de terceiros para desenvolver soluções que chamam MAPI. Observe que os desenvolvedores devem usar C ou C++não gerenciado, mas não C++ gerenciado para escrever soluções MAPI.
  
Quando um objeto MAPI é implementado, um cliente ou provedor de serviços cria código para todos os métodos de interface, código para quaisquer métodos privados específicos para a implementação e código para dar suporte a membros de dados privados para manter informações de estado. O código para os métodos de interface deve seguir as especificações publicadas pelo MAPI que documentam o comportamento esperado. 
  
Há muitas macros no arquivo de header Mapidefs.h e nos arquivos de header OLE que os clientes e provedores de serviços em qualquer idioma podem usar para ajudá-los com suas definições de objetos MAPI. Por exemplo, há uma macro para definir os métodos de cada uma das interfaces MAPI. A macro para definir os métodos da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) aparece em Mapidefs.h da seguinte forma: 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a>Confira também



[Visão geral de objetos e interface MAPI](mapi-object-and-interface-overview.md)

