---
title: Implementar objetos MAPI
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
# <a name="implementing-mapi-objects"></a>Implementar objetos MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os objetos MAPI podem ser implementados usando classes C++ ou estruturas de dados C, dependendo do idioma e do conjunto de APIs que um cliente ou provedor de serviços está usando. Os provedores de serviços podem ser escritos em C ou C++ com a interface do provedor de serviços MAPI; os aplicativos cliente também podem usar C ou C++. Se possível, os clientes e provedores de serviço que usam a interface de programação orientada a objeto devem usar C++. 
  
O C++ é a escolha preferida porque MAPI é uma tecnologia orientada a objeto e o C++ presta-se mais prontamente ao desenvolvimento orientado a objeto. O código resultante é mais simples e mais simples, facilitando a manutenção. A documentação MAPI é escrita principalmente para desenvolvedores do C++; todas as descrições de sintaxe dos métodos de interface MAPI nesta referência estão em C++.
  
Os desenvolvedores podem usar o Microsoft Visual Studio e ferramentas de desenvolvimento de terceiros para desenvolver soluções que chamam MAPI. Observe que os desenvolvedores devem usar o C++ C ou não gerenciado, mas não o C++ para escrever soluções MAPI.
  
Quando um objeto MAPI é implementado, um cliente ou provedor de serviços cria código para todos os métodos de interface, código para qualquer método privado específico da implementação e código para dar suporte a membros de dados privados para manter informações de estado. O código dos métodos de interface deve seguir as especificações publicadas por MAPI que documentam o comportamento esperado. 
  
Há muitas macros no arquivo de cabeçalho mapidefs. h e arquivos de cabeçalho OLE que os clientes e provedores de serviço em qualquer idioma podem usar para ajudá-los com suas definições de objetos MAPI. Por exemplo, há uma macro para definir os métodos de cada uma das interfaces MAPI. A macro para definir os métodos da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) aparece em mapidefs. h da seguinte maneira: 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a>Confira também



[Visão geral de interface e objeto MAPI](mapi-object-and-interface-overview.md)

