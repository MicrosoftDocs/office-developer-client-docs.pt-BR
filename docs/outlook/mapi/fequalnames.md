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
ms.openlocfilehash: 09c6540f2a224b7dc89a62c34cfb0c867cef4632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570846"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Determina se o MAPI duas propriedades nomeadas são os mesmos. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a>Parâmetros

 _lpName1_
  
> [in] Ponteiro para uma estrutura [MAPINAMEID](mapinameid.md) descrevendo a primeira propriedade nomeada. 
    
 _lpName2_
  
> [in] Ponteiro para uma estrutura **MAPINAMEID** descrevendo a segunda propriedade nomeada. 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> Os nomes das duas propriedades são iguais. 
    
FALSO 
  
> Os nomes das duas propriedades não são iguais.
    
## <a name="remarks"></a>Comentários

A função **FEqualNames** é útil porque a estrutura **MAPINAMEID** contém um [GUID](guid.md) e pode representar o próprio nome de propriedade em mais de uma forma. Isso significa que as duas estruturas não podem ser comparadas pelos métodos binários simples. 
  
O processo de teste diferencia maiusculas de minúsculas para as cadeias de caracteres de nome de propriedade. 
  

