---
title: Conjuntos de caracteres MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 898883d8c93b69762883a502b7a4313b3417d0d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319072"
---
# <a name="mapi-character-sets"></a>Conjuntos de caracteres MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos cliente compatíveis com MAPI e provedores de serviços podem usar caracteres ANSI (byte único) ou caracteres Unicode (byte duplo). Não há suporte para conjuntos de caracteres OEM. Uma cadeia de caracteres OEM passada para um método ou função MAPI causará falha no método ou na função. Os aplicativos cliente que funcionam com nomes de fileno conjunto de caracteres OEM devem ser cuidadoso para convertê-los em ANSI antes de passá-los para um método ou função MAPI.
  
O suporte ao conjunto de caracteres Unicode é opcional, tanto para clientes quanto para provedores de serviços. Todos os provedores de serviços devem gravar seu código para que eles possam compilar independentemente de terem ou não suporte Unicode. Os clientes são compilados condicionalmente, dependendo do nível de suporte, mas os provedores de serviços não. Eles não devem ter que ser recompilados quando o conjunto de caracteres é alterado. Nada no código do provedor de serviços deve ser condicional. 
  
Quando clientes ou provedores de serviço que oferecem suporte a Unicode fazem uma chamada de método que inclui cadeias de caracteres como parâmetros de entrada ou saída, eles definem o sinalizador MAPI_UNICODE. A definição desse sinalizador indica a implementação de que todas as cadeias de caracteres de entrada são cadeias de caracteres Unicode. Na saída, a definição desse sinalizador solicita que todas as cadeias de caracteres passadas da implementação devem ser cadeias de caracteres Unicode, se possível. Implementadores de métodos que dão suporte a Unicode serão compatíveis com a solicitação; os implementadores de métodos que não oferecem suporte a Unicode não são compatíveis. As propriedades de cadeia de caracteres que não estão no formato Unicode são do tipo PT_STRING8.
  
MAPI define a constante **fMapiUnicode** no arquivo de cabeçalho MAPIDEFS. H para representar o conjunto de caracteres padrão. Se um cliente ou provedor de serviços oferecer suporte a Unicode, **fMapiUnicode** é definido como MAPI_UNICODE. Clientes e provedores de serviço que não dão suporte a Unicode Set **fMapiUnicode** como zero. 
  
Os provedores de serviços que não dão suporte ao Unicode devem:
  
- Recusar a execução de conversões entre conjuntos de caracteres.
    
- Nunca passe o sinalizador MAPI_UNICODE em chamadas de método.
    
- Retornar MAPI_E_BAD_CHARWIDTH quando o sinalizador MAPI_UNICODE for passado.
    
- Declare explicitamente as propriedades da cadeia de caracteres ANSI. 
    
Os provedores de serviços também podem retornar MAPI_E_BAD_CHARWIDTH quando só dão suporte a Unicode e clientes não passam o sinalizador MAPI_UNICODE. 
  
 A versão atual do MAPI oferece suporte a Unicode nos seguintes métodos: 
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
  
[IAddrBook::Details](iaddrbook-details.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPIProp:: GetLastError](imapiprop-getlasterror.md) (Apenas implementação do**IAddrBook** ) 
  
Para esses métodos, os chamadores podem esperar que qualquer cadeia de caracteres retornada seja cadeia de caracteres Unicode. As cadeias de caracteres retornadas de implementações MAPI de qualquer outro método serão cadeias de caracteres ANSI.
  

