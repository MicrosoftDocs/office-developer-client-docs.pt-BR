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
ms.openlocfilehash: 90829f8fff530d22a7dee68dc227655064147cee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575326"
---
# <a name="stnefproblem"></a>STnefProblem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém informações sobre um problema de processamento de propriedade ou atributo que ocorreram durante a codificação ou decodificação de um stream TNEF Transport Neutral Encapsulation Format ().
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |TNEF.h  <br/> |
   
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
  
> O tipo de processamento durante o qual o problema ocorreu. Se o problema ocorreu durante o processamento de mensagens, o membro **ulComponent** é definido como zero. Se o problema ocorreu durante o processamento de anexo, **ulComponent** é definido igual ao valor de **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo correspondente.
    
 **ulAttribute**
  
> Atributo associado à propriedade indicada pelo membro **ulPropTag** ou, quando o problema de processamento TNEF ocorre quando um encapsulamento de decodificação bloquear, um dos seguintes valores: 
    
 _attMAPIProps_
  
> Nível de mensagem
    
 _attAttachment_
  
> Nível de anexo
    
 **ulPropTag**
  
> Marca de propriedade da propriedade que causou o problema de processamento TNEF, exceto quando o problema ocorre quando um bloco de encapsulamento no qual maiusculas **ulPropTag** é definido como zero de decodificação. 
    
 **SCODE**
  
> Valor de erro indicando que o problema encontrado durante o processamento.
    
## <a name="remarks"></a>Comentários

Se uma estrutura de **STnefProblem** não foi gerada durante o processamento de um atributo ou propriedade, o aplicativo pode continuar com a pressuposição de que o processamento desse atributo ou a propriedade teve êxito. A única exceção ocorre quando o problema surgiu durante a decodificação de um bloco de encapsulamento. Nesse caso, o componente correspondente para o bloco de decodificação é interrompido e decodificação continua no outro componente. 
  
## <a name="see-also"></a>Confira também



[STnefProblemArray](stnefproblemarray.md)
  
[Propriedade canônica PidTagAttachNumber](pidtagattachnumber-canonical-property.md)


[Estruturas MAPI](mapi-structures.md)

