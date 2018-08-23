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
ms.openlocfilehash: 8002698b1644fb63292b4242d4fb3d784a99a03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592021"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Multiplica um inteiro não assinado de 32 bits por outro.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>Parâmetros

 _Multiplicand_
  
> [in] Uma palavra dupla que contém o inteiro não assinado de 32 bits seja multiplicado pelo valor no parâmetro _multiplicador_ . 
    
 _Multiplicador_
  
> [in] Uma palavra dupla que contém o multiplicador de inteiro não assinado de 32 bits.
    
## <a name="return-value"></a>Valor retornado

A função **FtMulDwDw** retorna uma estrutura [FILETIME](filetime.md) que contém o produto dos dois valores inteiros. Os dois parâmetros de entrada permanecem inalterados. 
  

