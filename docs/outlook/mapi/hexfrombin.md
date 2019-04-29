---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a1bf02de914865e27c8c018aba8695c858888ae2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412573"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Converte um número binário em uma representação de cadeia de caracteres de um número hexadecimal. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a>Parâmetros

 _pb_
  
> no Ponteiro para os dados binários a serem convertidos. 
    
 _cb_
  
> no Tamanho, em bytes, dos dados binários apontados pelo parâmetro _PB_ . 
    
 _v_
  
> bota Ponteiro para uma cadeia de caracteres ASCII terminada em nulo que representa os dados binários em dígitos hexadecimais.
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

A função **HexFromBin** usa um ponteiro para uma unidade de dados binários cujo tamanho é indicado pelo parâmetro _CB_ . Ele retorna na cadeia de caracteres _sz_ , dentro (2 * _CB_) + 1 bytes de memória, uma representação dessas informações binárias em números hexadecimais. Se o valor de byte for Decimal 10, por exemplo, a cadeia de caracteres hexadecimal será 0A, então um byte é convertido em dois bytes na cadeia de caracteres. 
  

