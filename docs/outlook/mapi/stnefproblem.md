---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 19d20a3fb06f6a0a0671ba4bfd938da314001778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435177"
---
# <a name="stnefproblem"></a>STnefProblem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém informações sobre um problema de processamento de propriedade ou de atributo que ocorreu durante a codificação ou a decodificação de um fluxo TNEF (Transport neutral Encapsulation Format).
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |TNEF. h  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a>Members

 **ulComponent**
  
> O tipo de processamento durante o qual o problema ocorreu. Se o problema ocorreu durante o processamento de mensagens, o membro **ulComponent** é definido como zero. Se o problema ocorreu durante o processamento de anexos, **ulComponent** é definido como igual ao valor de **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo correspondente.
    
 **ulAttribute**
  
> Atributo associado à propriedade indicada pelo membro **ulPropTag** ou, quando o problema de processamento TNEF ocorre ao decodificar um bloco de encapsulamento, um dos seguintes valores: 
    
 _attMAPIProps_
  
> Nível de mensagem
    
 _attAttachment_
  
> Nível de anexo
    
 **ulPropTag**
  
> Marca de propriedade da propriedade que causou o problema de processamento TNEF, exceto quando o problema ocorre ao decodificar um bloco de encapsulamento, nesse caso, **ulPropTag** é definido como zero. 
    
 **SCODE**
  
> O valor de erro que indica o problema encontrado durante o processamento.
    
## <a name="remarks"></a>Comentários

Se uma estrutura **STnefProblem** não for gerada durante o processamento de um atributo ou propriedade, o aplicativo poderá continuar sob a pressuposição de que o processamento desse atributo ou propriedade foi bem-sucedido. A única exceção ocorre quando o problema surgiu durante a decodificação de um bloco de encapsulamento. Nesse caso, a decodificação do componente correspondente ao bloco é interrompida e a decodificação continua em outro componente. 
  
## <a name="see-also"></a>Confira também



[STnefProblemArray](stnefproblemarray.md)
  
[Propriedade canônica PidTagAttachNumber](pidtagattachnumber-canonical-property.md)


[Estruturas MAPI](mapi-structures.md)

