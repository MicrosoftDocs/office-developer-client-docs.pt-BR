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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417550"
---
# <a name="mapi-character-sets"></a>Conjuntos de caracteres MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Aplicativos cliente e provedores de serviços compatíveis com MAPI podem usar caracteres ANSI (byte único) ou caracteres Unicode (byte duplo). Não há suporte para conjuntos de caracteres OEM. Uma cadeia de caracteres OEM passada para um método ou função MAPI causará falha nesse método ou função. Os aplicativos cliente que trabalham com nomes de arquivo no conjunto de caracteres OEM devem ter cuidado para convertê-los em ANSI antes de passá-los para um método ou função MAPI.
  
O suporte ao conjunto de caracteres Unicode é opcional, tanto para clientes quanto para provedores de serviços. Todos os provedores de serviços devem escrever seu código para que possam compilar independentemente de eles suportarem ou não Unicode. Os clientes compilam condicionalmente, dependendo do nível de suporte, mas os provedores de serviços não. Eles não devem ter que ser recompilados quando o conjunto de caracteres muda. Nada no código do provedor de serviços deve ser condicional. 
  
Quando clientes ou provedores de serviços que suportam Unicode fazem uma chamada de método que inclui cadeias de caracteres como parâmetros de entrada ou saída, eles configuram o sinalizador MAPI_UNICODE caracteres. Definir esse sinalizador indica à implementação que todas as cadeias de caracteres de entrada são cadeias de caracteres Unicode. Na saída, a definição desse sinalizador solicita que todas as cadeias de caracteres passadas da implementação sejam cadeias de caracteres Unicode, se possível. Implementadores de método que suportam Unicode atenderão à solicitação; implementadores de método que não oferecem suporte a Unicode não estarão em conformidade. Propriedades de cadeia de caracteres que não estão no formato Unicode são do tipo PT_STRING8.
  
MAPI define a **constante fMapiUnicode** no arquivo de header MAPIDEFS. H para representar o conjunto de caracteres padrão. Se um cliente ou provedor de serviços suportar Unicode, **fMapiUnicode** será definido como MAPI_UNICODE. Clientes e provedores de serviços que não suportam o conjunto **de unicode fMapiUnicode** como zero. 
  
Os provedores de serviços que não suportam Unicode devem:
  
- Recusa-se a executar conversões entre conjuntos de caracteres.
    
- Nunca passe o sinalizador MAPI_UNICODE em chamadas de método.
    
- Retornar MAPI_E_BAD_CHARWIDTH quando o MAPI_UNICODE de dados for passado.
    
- Declare explicitamente as propriedades da cadeia de caracteres ANSI. 
    
Os provedores de serviços também podem retornar MAPI_E_BAD_CHARWIDTH quando só suportam Unicode e os clientes não passam o sinalizador MAPI_UNICODE dados. 
  
 A versão atual do MAPI dá suporte a Unicode nos seguintes métodos: 
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
  
[IAddrBook::Details](iaddrbook-details.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**somente implementação de IAddrBook)** 
  
Para esses métodos, os chamadores podem esperar que todas as cadeias de caracteres retornadas sejam cadeias de caracteres Unicode. Cadeias de caracteres retornadas de implementações MAPI de qualquer outro método serão cadeias de caracteres ANSI.
  

