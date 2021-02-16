---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8f71b30bd02af8f768da86218456feadda8ea1b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414799"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Determina se duas propriedades nomeadas MAPI são iguais. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a>Parâmetros

 _lpName1_
  
> [in] Ponteiro para uma [estrutura MAPINAMEID que](mapinameid.md) descreve a primeira propriedade nomeada. 
    
 _lpName2_
  
> [in] Ponteiro para uma **estrutura MAPINAMEID que** descreve a segunda propriedade nomeada. 
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> Os dois nomes de propriedade são iguais. 
    
FALSE 
  
> Os dois nomes de propriedade não são iguais.
    
## <a name="remarks"></a>Comentários

A **função FEqualNames** é útil porque a estrutura **MAPINAMEID** contém um [GUID](guid.md) e pode representar o nome da propriedade em si de mais de uma maneira. Isso significa que as duas estruturas não podem ser comparadas por métodos binários simples. 
  
O processo de teste faz a seleção de caso para as cadeias de caracteres do nome da propriedade. 
  

