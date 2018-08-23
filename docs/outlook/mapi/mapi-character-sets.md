---
title: Conjuntos de caracteres MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5f7da3da8d23b28e13c39570b8f5971cb75a3310
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582529"
---
# <a name="mapi-character-sets"></a>Conjuntos de caracteres MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Provedores de serviços e aplicativos cliente compatíveis com MAPI podem usar caracteres ANSI (byte único) ou caracteres Unicode (byte duplo). Não há suporte para conjuntos de caracteres OEM. Uma cadeia de OEM passado a um método MAPI ou função fará com que esse método ou função falha. Aplicativos de cliente que funcionam com nomes de arquivo no conjunto de caracteres OEM devem tomar cuidadosos convertê-los para ANSI antes de passá-los para uma função ou um método MAPI.
  
Conjunto de caracteres com suporte o Unicode é opcional, tanto para clientes e provedores de serviços. Todos os provedores de serviço devem escrever seu código para que eles podem compilar independentemente de estarem ou não eles oferecem suporte a Unicode. Clientes Compilar condicionalmente, dependendo do seu nível de suporte, mas não provedores de serviços. Eles não precisará ser recompilado quando o conjunto de caracteres alterações. Nada no código do provedor de serviço deve ser condicional. 
  
Quando clientes ou provedores de serviço que oferecem suporte a Unicode fazer uma chamada de método que inclui as sequências de caracteres como parâmetros de entrada ou saídas, eles definido o sinalizador MAPI_UNICODE. Defina esse sinalizador indica feitas na implementação, que todas as cadeias de caracteres de entrada são cadeias de caracteres Unicode. Na saída, definir este sinalizador solicitações que todas as cadeias de caracteres passadas de volta a partir da implementação deve ser cadeias de caracteres Unicode se possível. Implementadores de método que ofereça suporte a Unicode cumprirá a solicitação; não estejam em conformidade implementadores de método que não oferecem suporte a Unicode. Propriedades de cadeia de caracteres que não estão no formato Unicode são do tipo PT_STRING8.
  
MAPI define a constante **fMapiUnicode** no arquivo de cabeçalho MAPIDEFS. H para representar o conjunto de caracteres padrão. Se um cliente ou serviço provedor oferece suporte a Unicode, **fMapiUnicode** é definido como MAPI_UNICODE. Clientes e provedores de serviços que não oferecem suporte a Unicode defina **fMapiUnicode** como zero. 
  
Provedores de serviços que não oferecem suporte a Unicode devem:
  
- Recuse executar conversões entre conjuntos de caracteres.
    
- Nunca passe o sinalizador MAPI_UNICODE em chamadas de método.
    
- Retorne MAPI_E_BAD_CHARWIDTH quando o sinalizador MAPI_UNICODE é passado.
    
- Declare explicitamente o propriedades de cadeia de caracteres ANSI. 
    
Provedores de serviços também podem retornar MAPI_E_BAD_CHARWIDTH quando eles só oferecem suporte a Unicode e os clientes não passar o sinalizador MAPI_UNICODE. 
  
 A versão atual do MAPI oferece suporte a Unicode nos seguintes métodos: 
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
  
[IAddrBook::Details](iaddrbook-details.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (Somente para a implementação**IAddrBook** ) 
  
Para esses métodos, os chamadores podem esperar qualquer cadeia de caracteres retornada como sequências de caracteres Unicode. Cadeias de caracteres retornadas de implementações de MAPI de qualquer outro método será cadeias de caracteres ANSI.
  

