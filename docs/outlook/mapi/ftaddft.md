---
title: FtAddFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtAddFt
api_type:
- COM
ms.assetid: 341ad06b-1caa-49bb-b859-cb512f6fb55d
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: e0e1535a770d4f1b437faf6a90c5f6415f6000ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766635"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**Aplica-se a**: Outlook 
  
Adiciona um inteiro não assinado de 64 bits para outro.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a>Par�metros

 _Addend1_
  
> [in] Uma estrutura [FILETIME](filetime.md) que contém o primeiro inteiro não assinado de 64 bits a ser adicionado. 
    
 _Addend2_
  
> [in] Uma estrutura **FILETIME** que contém o segundo inteiro não assinado de 64 bits a ser adicionado. 
    
## <a name="return-value"></a>Valor retornado

A função **FtAddFt** retorna uma estrutura **FILETIME** que contém a soma dos dois valores inteiros. Os dois parâmetros de entrada permanecem inalterados. 
  

