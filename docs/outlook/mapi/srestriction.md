---
title: SRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRestriction
api_type:
- COM
ms.assetid: c12b4409-da6f-480b-87af-1e5baea2e8bd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5f8a76cb317ac9bf1b6a4dc4a92b6d6f0098e1d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577398"
---
# <a name="srestriction"></a>SRestriction

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um filtro para limitar o modo de exibição de uma tabela às linhas específicas. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SRestriction
{
  ULONG rt;
  union
  {
    SComparePropsRestriction resCompareProps;
    SAndRestriction resAnd;
    SOrRestriction resOr;
    SNotRestriction resNot;
    SContentRestriction resContent;
    SPropertyRestriction resProperty;
    SBitMaskRestriction resBitMask;
    SSizeRestriction resSize;
    SExistRestriction resExist;
    SSubRestriction resSub;
    SCommentRestriction resComment;
  } res;
} SRestriction;

```

## <a name="members"></a>Members

 **RT**
  
> O tipo de restrição. Os valores possíveis são: 
    
RES_AND 
  
> Uma restrição **AND** , que se aplica a uma operação de **AND** bit a bit a uma restrição. 
    
RES_BITMASK 
  
> Uma restrição de bitmask que se aplica a uma máscara de bits para um valor de propriedade.
    
RES_COMMENT 
  
> Uma restrição de comentário, que associa um comentário uma restrição.
    
RES_COMPAREPROPS 
  
> Uma restrição de comparação de propriedade, que compara dois valores de propriedade.
    
RES_CONTENT 
  
> Uma restrição de conteúdo, que procura um valor de propriedade para conteúdo específico.
    
RES_EXIST 
  
> Uma restrição da lista, que determina se uma propriedade é suportada.
    
RES_NOT 
  
> Uma **não** restrição, que se aplica a uma operação **não é** lógica para uma restrição. 
    
RES_OR 
  
> Uma restrição **ou** , que se aplica a uma operação **OR** lógica para uma restrição. 
    
RES_PROPERTY 
  
> Uma restrição de propriedade, que determina se um valor da propriedade corresponde a um determinado valor.
    
RES_SIZE 
  
> Uma restrição de tamanho, que determina se um valor de propriedade é de um determinado tamanho.
    
RES_SUBRESTRICTION 
  
> Uma restrição de objeto sub, que se aplica a uma restrição de anexos ou os destinatários de uma mensagem.
    
 **res**
  
> União de estruturas de restrição descrevendo o filtro a ser aplicado. A estrutura específica incluída no membro **rec** depende do valor do membro **rt** . O mapeamento entre o tipo de restrição e a estrutura está listado na tabela a seguir. 
    
|||
|:-----|:-----|
|**Tipo de restrição** <br/> |**Estrutura de restrição** <br/> |
|RES_AND  <br/> |[SAndRestriction](sandrestriction.md) <br/> |
|RES_BITMASK  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |
|RES_COMMENT  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |
|RES_COMPAREPROPS  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |
|RES_CONTENT  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |
|RES_EXIST  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |
|RES_NOT  <br/> |[SNotRestriction](snotrestriction.md) <br/> |
|RES_OR  <br/> |[SOrRestriction](sorrestriction.md) <br/> |
|RES_PROPERTY  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |
|RES_SIZE  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |
|RES_SUBRESTRICTION  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a>Comentários

Os clientes usar uma estrutura **SRestriction** para limitar o número e tipo de linhas no seu modo de exibição de uma tabela e procurar mensagens específicas em uma pasta. Para impor a limitação em uma tabela, os clientes chamam [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md). Para impor a limitação em uma pasta, clientes chamar o método de [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) da pasta. 
  
Para obter informações sobre como usar as restrições com tabelas, consulte [Sobre restrições](about-restrictions.md). 
  
## <a name="see-also"></a>Confira também



[SAndRestriction](sandrestriction.md)
  
[SBitMaskRestriction](sbitmaskrestriction.md)
  
[SCommentRestriction](scommentrestriction.md)
  
[SComparePropsRestriction](scomparepropsrestriction.md)
  
[SContentRestriction](scontentrestriction.md)
  
[SExistRestriction](sexistrestriction.md)
  
[SNotRestriction](snotrestriction.md)
  
[SOrRestriction](sorrestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SSizeRestriction](ssizerestriction.md)
  
[SSubRestriction](ssubrestriction.md)


[Estruturas MAPI](mapi-structures.md)

