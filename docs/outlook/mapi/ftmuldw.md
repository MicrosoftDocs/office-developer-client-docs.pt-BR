---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 27ec919d720e1089d6e102f20485d936c9dc9808
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327997"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Multiplica um inteiro de 64 bits não assinado por um inteiro de 32 bits não assinado.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a>Parâmetros

 _Multiplicador_
  
> no Uma palavra dupla que contém o multiplicador inteiro de 32 bits não assinado. 
    
 _Multiplicand_
  
> no Uma estrutura [FILETIME](filetime.md) que contém o inteiro de 64 bits não assinado a ser multiplicado pelo valor no parâmetro multiplicador __ . 
    
## <a name="return-value"></a>Valor de retorno

A função **FtMulDw** retorna uma estrutura **FILETIME** que contém o produto dos dois números inteiros. Os dois parâmetros de entrada permanecem inalterados. 
  

