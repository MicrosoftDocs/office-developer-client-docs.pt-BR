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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 861a48464193f357224e33eb0348bc7d5372aa10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766628"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**Aplica-se a**: Outlook 
  
Multiplica um inteiro de 64 bits não assinado por um inteiro não assinado de 32 bits.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a>Par�metros

 _Multiplicador_
  
> [in] Uma palavra dupla que contém o multiplicador de inteiro não assinado de 32 bits. 
    
 _Multiplicand_
  
> [in] Uma estrutura [FILETIME](filetime.md) que contém o inteiro não assinado de 64 bits seja multiplicado pelo valor no parâmetro _multiplicador_ . 
    
## <a name="return-value"></a>Valor retornado

A função **FtMulDw** retorna uma estrutura **FILETIME** que contém o produto dos dois valores inteiros. Os dois parâmetros de entrada permanecem inalterados. 
  

