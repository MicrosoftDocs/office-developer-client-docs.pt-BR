---
title: FtMulDwDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDwDw
api_type:
- COM
ms.assetid: 8c1a342c-d7ae-4e26-b327-a63cdd3c3ee6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 54561450e7d91d8a30695dacf508758623547e39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412909"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Multiplica um inteiro de 32 bits não assinado por outro.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>Parâmetros

 _Multiplicand_
  
> no Uma palavra dupla que contém o inteiro de 32 bits não assinado a ser multiplicado pelo valor no parâmetro multiplicador __ . 
    
 _Multiplicador_
  
> no Uma palavra dupla que contém o multiplicador inteiro de 32 bits não assinado.
    
## <a name="return-value"></a>Valor de retorno

A função **FtMulDwDw** retorna uma estrutura [FILETIME](filetime.md) que contém o produto dos dois números inteiros. Os dois parâmetros de entrada permanecem inalterados. 
  

