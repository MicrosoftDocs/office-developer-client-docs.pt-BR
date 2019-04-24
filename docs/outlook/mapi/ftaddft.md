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
ms.openlocfilehash: cb20469adec938817fedf1b00789304625b388c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328004"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona um inteiro de 64 bits não assinado a outro.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a>Parâmetros

 _Addend1_
  
> no Uma estrutura [FILETIME](filetime.md) que contém o primeiro inteiro de 64 bits não assinado a ser adicionado. 
    
 _Addend2_
  
> no Uma estrutura **FILETIME** que contém o segundo inteiro não assinado de 64 bits a ser adicionado. 
    
## <a name="return-value"></a>Valor de retorno

A função **FtAddFt** retorna uma estrutura **FILETIME** que contém a soma dos dois inteiros. Os dois parâmetros de entrada permanecem inalterados. 
  

