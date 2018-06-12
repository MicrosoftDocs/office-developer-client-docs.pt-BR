---
title: Implementar objetos de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d53304dd74a0e54974d479c66637079cd48b2fc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767423"
---
# <a name="implementing-mapi-objects"></a>Implementar objetos de MAPI

  
  
**Aplica-se a**: Outlook 
  
Objetos MAPI podem ser implementados usando classes C++ ou C estruturas de dados, dependendo do idioma e a API definido um cliente ou usando o provedor de serviços. Provedores de serviço podem ser escritos em C ou C++ com a interface do provedor de serviços MAPI; aplicativos cliente também podem usar C ou C++. Se possível, clientes e provedores de serviços que usam a interface de programação orientado a objetos devem usar C++. 
  
C++ é a opção preferida porque MAPI é uma tecnologia orientada e C++ presta mais prontamente a desenvolvimento orientado a objetos. O código resultante é mais simples e mais ágil, facilitando a manutenção. A documentação de MAPI foi escrita principalmente para desenvolvedores de C++; todas as descrições de sintaxe para os métodos de interface MAPI nesta referência estão em C++.
  
Os desenvolvedores podem usar o Microsoft Visual Studio e ferramentas de desenvolvimento de terceiros para desenvolver soluções que chamam MAPI. Observe que os desenvolvedores devem usar C ou C++ não gerenciado, mas não gerenciadas do C++ para gravar as soluções MAPI.
  
Quando um objeto MAPI é implementado, um provedor de cliente ou serviço cria código para todos os métodos de interface, o código para quaisquer métodos privados que são específicas para a implementação e o código para dar suporte a membros de dados particulares para manutenção de informações de estado. O código para os métodos de interface deve seguir as especificações publicadas pela MAPI que documentam o comportamento esperado. 
  
Há muitas macros no arquivo de cabeçalho Mapidefs.h e arquivos de cabeçalho OLE que os clientes e provedores de serviços em qualquer idioma podem usar para ajudá-los com suas definições de objetos MAPI. Por exemplo, há uma macro para definir os métodos de cada uma das interfaces de MAPI. A macro para definir os métodos da interface [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) aparece no Mapidefs.h da seguinte maneira: 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a>Confira também



[Objeto MAPI e visão geral da Interface](mapi-object-and-interface-overview.md)

