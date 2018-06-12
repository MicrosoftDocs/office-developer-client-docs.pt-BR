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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 8595cdb411e68f2aed3ac063b2b81965e9b4d975
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770516"
---
# <a name="stnefproblem"></a>STnefProblem

  
  
**Aplica-se a**: Outlook 
  
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

## <a name="members"></a>Membros

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
    
## <a name="remarks"></a>Coment�rios

Se uma estrutura de **STnefProblem** não foi gerada durante o processamento de um atributo ou propriedade, o aplicativo pode continuar com a pressuposição de que o processamento desse atributo ou a propriedade teve êxito. A única exceção ocorre quando o problema surgiu durante a decodificação de um bloco de encapsulamento. Nesse caso, o componente correspondente para o bloco de decodificação é interrompido e decodificação continua no outro componente. 
  
## <a name="see-also"></a>Confira também



[STnefProblemArray](stnefproblemarray.md)
  
[Propriedade canônico de PidTagAttachNumber](pidtagattachnumber-canonical-property.md)


[Estruturas MAPI](mapi-structures.md)

