---
title: SMAPIFormProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormProp
api_type:
- COM
ms.assetid: 80f1c2e0-3567-4b16-86cb-d5e6ac95c2ee
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4e8e2474d2adb882dd0ba43aeb0d8b05044a6ce6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592056"
---
# <a name="smapiformprop"></a>SMAPIFormProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma propriedade nomeada utilizada com um formulário. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
   
```cpp
typedef struct _SMAPIFormProp
{
  ULONG ulFlags;
  ULONG nPropType;
  MAPINAMEID nmid;
  LPSTR pszDisplayName;
  FORMPROPSPECIALTYPE nSpecialType;
  union
  {
    struct
    {
      MAPINAMEID nmidIdx;
      ULONG cfpevAvailable;
      LPMAPIFORMPROPENUMVAL pfpevAvailable;
    } s1;
  } u;
} SMAPIFormProp, FAR * LPMAPIFORMPROP;

```

## <a name="members"></a>Members

 **ulFlags**
  
> Sinalizadores usados para distinguir o formato das cadeias de caracteres na estrutura **SMAPIFormProp** . O seguinte sinalizador pode ser definido: 
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas estão no formato Unicode. Se MAPI_UNICODE não estiver definida, as cadeias de caracteres estão no formato ANSI.
    
 **nPropType**
  
> Tipo da propriedade nomeado, com a palavra mais significativa definida como zero. 
    
 **nmid**
  
> Nome da propriedade nomeada, que inclui uma estrutura **GUID** que identifica o valor da propriedade set e um numérico ou cadeia de caracteres que representa um nome de formulário e de identificador de interface. 
    
 **pszDisplayName**
  
> Ponteiro para o nome para exibição da propriedade nomeada.
    
 **nSpecialType**
  
> Valor que descreve o tipo de dados incluídos no membro **u** . Os valores possíveis são: 
    
FPST_VANILLA 
  
> O membro **u** não contiver uma enumeração. 
    
FPST_ENUM_PROP 
  
> O membro **u** contém uma estrutura que descreve uma enumeração. 
    
 **u**
  
> União descrevendo a associação entre o nome e o número da propriedade nomeada. Usando algumas propriedades, o membro **u** está vazio. Com outras propriedades, ele é representado em uma estrutura que consiste dos seguintes membros: 
    
 **nmidIdx**
  
> A estrutura [MAPINAMEID](mapinameid.md) que contém o conjunto de propriedades e o identificador para a propriedade nomeada. 
    
 **cfpevAvailable**
  
> Contagem de estruturas de [SMAPIFormPropEnumVal](smapiformpropenumval.md) na matriz apontado pelo membro **pfpevAvailable** . 
    
 **pfpevAvailable**
  
> Ponteiro para uma matriz de estruturas de **SMAPIFormPropEnumVal** , cada um dos quais mantém um valor para a propriedade nomeada. 
    
## <a name="remarks"></a>Comentários

A estrutura de **SMAPIFormProp** contém informações sobre uma propriedade de formulário usada como parte das definições de interface do [IMAPIFormInfo](imapiforminfoimapiprop.md) ; **nSpecialType** contém uma marca que se aplica a união **u** que faz parte do **SMAPIFormProp**.
  
## <a name="see-also"></a>Confira também



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[Estruturas MAPI](mapi-structures.md)

