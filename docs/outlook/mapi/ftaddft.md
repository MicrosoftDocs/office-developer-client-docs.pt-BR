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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4b02fc316001ae11d64988cc29d0e62e9adde55e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585581"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parâmetros

 _Addend1_
  
> [in] Uma estrutura [FILETIME](filetime.md) que contém o primeiro inteiro não assinado de 64 bits a ser adicionado. 
    
 _Addend2_
  
> [in] Uma estrutura **FILETIME** que contém o segundo inteiro não assinado de 64 bits a ser adicionado. 
    
## <a name="return-value"></a>Valor retornado

A função **FtAddFt** retorna uma estrutura **FILETIME** que contém a soma dos dois valores inteiros. Os dois parâmetros de entrada permanecem inalterados. 
  

