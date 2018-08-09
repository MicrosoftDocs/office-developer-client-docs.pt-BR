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
ms.openlocfilehash: c1d333c7c019c30c3f6c6b3567453f2f022d4b5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766728"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**Aplica-se a**: Outlook 
  
Converte um número binário em uma representação de cadeia de caracteres de um número hexadecimal. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a>Parâmetros

 _pb_
  
> [in] Ponteiro para os dados binários a ser convertido. 
    
 _cb_
  
> [in] Tamanho, em bytes, dos dados binários apontado pelo parâmetro _pb_ . 
    
 _SZ_
  
> [out] Ponteiro para uma cadeia de ASCII terminada em nulo, que representa os dados binários em dígitos hexadecimais.
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

A função **HexFromBin** usa um ponteiro para uma unidade de dados binários cujo tamanho é indicado pelo parâmetro _cb_ . Ele retorna na cadeia de caracteres _sz_ contido em (2 * _cb_) + 1 bytes de memória, uma representação dessas informações binárias em hexadecimais números. Se o valor de byte é 10 decimal, por exemplo, a cadeia de caracteres hexadecimal será 0A, um byte caso se converte na cadeia de caracteres de dois bytes. 
  

