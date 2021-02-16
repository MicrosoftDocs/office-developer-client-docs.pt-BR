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
ms.openlocfilehash: a2a6d273495df52adb83393dc5549b0872c8f6f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439356"
---
# <a name="srestriction"></a>SRestriction

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um filtro para limitar a exibição de uma tabela a linhas específicas. 
  
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

 **rt**
  
> O tipo de restrição. Os valores possíveis são: 
    
RES_AND 
  
> Uma **restrição AND,** que se aplica a uma operação **AND** bit a bit a uma restrição. 
    
RES_BITMASK 
  
> Uma restrição de bitmask, que aplica uma máscara de bits a um valor de propriedade.
    
RES_COMMENT 
  
> Uma restrição de comentário, que associa um comentário a uma restrição.
    
RES_COMPAREPROPS 
  
> Uma restrição de comparação de propriedade, que compara dois valores de propriedade.
    
RES_CONTENT 
  
> Uma restrição de conteúdo, que pesquisa um valor de propriedade para conteúdo específico.
    
RES_EXIST 
  
> Uma restrição existente, que determina se uma propriedade é suportada.
    
RES_NOT 
  
> Uma **restrição NOT,** que aplica uma operação **LÓGICA NOT** a uma restrição. 
    
RES_OR 
  
> Uma **restrição OR,** que aplica uma operação **OR** lógica a uma restrição. 
    
RES_PROPERTY 
  
> Uma restrição de propriedade, que determina se um valor de propriedade corresponde a um valor específico.
    
RES_SIZE 
  
> Uma restrição de tamanho, que determina se um valor de propriedade é um tamanho específico.
    
RES_SUBRESTRICTION 
  
> Uma restrição de subpro object, que aplica uma restrição a anexos ou destinatários de uma mensagem.
    
 **res**
  
> União de estruturas de restrição que descrevem o filtro a ser aplicado. A estrutura específica incluída no **membro res** depende do valor do **membro rt.** O mapeamento entre o tipo de restrição e a estrutura está listado na tabela a seguir. 
    
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

Os clientes usam **uma estrutura SRestriction** para limitar o número e o tipo de linhas em sua exibição de uma tabela e para pesquisar mensagens específicas em uma pasta. Para impor a limitação em uma tabela, os clientes chamam [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md). Para impor a limitação em uma pasta, os clientes chamam o método [IMAPIContainer::SetSearchCriteria da](imapicontainer-setsearchcriteria.md) pasta. 
  
Para obter informações sobre como usar restrições com tabelas, consulte [Sobre restrições.](about-restrictions.md) 
  
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

