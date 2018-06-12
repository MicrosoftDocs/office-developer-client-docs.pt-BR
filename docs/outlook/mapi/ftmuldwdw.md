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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 16dca82b94225afc88bcb6c4e698a50565d6b088
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766632"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**Aplica-se a**: Outlook 
  
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

## <a name="parameters"></a>Par�metros

 _Multiplicand_
  
> [in] Uma palavra dupla que contém o inteiro não assinado de 32 bits seja multiplicado pelo valor no parâmetro _multiplicador_ . 
    
 _Multiplicador_
  
> [in] Uma palavra dupla que contém o multiplicador de inteiro não assinado de 32 bits.
    
## <a name="return-value"></a>Valor retornado

A função **FtMulDwDw** retorna uma estrutura [FILETIME](filetime.md) que contém o produto dos dois valores inteiros. Os dois parâmetros de entrada permanecem inalterados. 
  

