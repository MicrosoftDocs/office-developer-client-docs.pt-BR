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
ms.openlocfilehash: 968f9e1dad3a233b31f0ce29d3ce935b1257948c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309496"
---
# <a name="smapiformprop"></a>SMAPIFormProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma propriedade nomeada usada com um formulário. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform. h  <br/> |
   
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

## <a name="members"></a>Membros

 **ulFlags**
  
> Sinalizadores usados para distinguir o formato das cadeias de caracteres na estrutura **SMAPIFormProp** . O seguinte sinalizador pode ser definido: 
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas estão no formato Unicode. Se MAPI_UNICODE não for definido, as cadeias de caracteres estarão no formato ANSI.
    
 **nPropType**
  
> Tipo da propriedade nomeada, com a palavra mais significativa definida como zero. 
    
 **nmid**
  
> Nome da propriedade nomeada, que inclui uma estrutura **GUID** que identifica o conjunto de propriedades e um valor numérico ou de cadeia de caracteres que representa um identificador de interface e um nome de formulário. 
    
 **pszDisplayName**
  
> Ponteiro para o nome de exibição da propriedade nomeada.
    
 **nSpecialType**
  
> Valor que descreve o tipo de dados incluído no membro **u** . Os valores possíveis são os seguintes: 
    
FPST_VANILLA 
  
> O membro **u** não contém uma enumeração. 
    
FPST_ENUM_PROP 
  
> O membro **u** contém uma estrutura que descreve uma enumeração. 
    
 **u**
  
> União descrevendo a associação entre o nome e o número da propriedade nomeada. Usando algumas propriedades, o membro **u** está vazio. Com outras propriedades, ela é representada em uma estrutura que consiste nos seguintes membros: 
    
 **nmidIdx**
  
> A estrutura [MAPINAMEID](mapinameid.md) que contém o conjunto de propriedades e o identificador da propriedade nomeada. 
    
 **cfpevAvailable**
  
> Contagem de estruturas [SMAPIFormPropEnumVal](smapiformpropenumval.md) na matriz apontada pelo membro **pfpevAvailable** . 
    
 **pfpevAvailable**
  
> Ponteiro para uma matriz de estruturas **SMAPIFormPropEnumVal** , cada uma delas armazena um valor para a propriedade named. 
    
## <a name="remarks"></a>Comentários

A estrutura **SMAPIFormProp** contém informações sobre uma propriedade de formulário usada como parte das definições da interface [IMAPIFormInfo](imapiforminfoimapiprop.md) ; **nSpecialType** contém uma marca que se aplica à União **u** que faz parte de **SMAPIFormProp**.
  
## <a name="see-also"></a>Confira também



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[Estruturas MAPI](mapi-structures.md)

