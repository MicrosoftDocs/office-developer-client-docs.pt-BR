---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 87a470c1c682225eb1deefba9ccc8c12fbdc49c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569824"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Converte uma representação de cadeia de caracteres de um número hexadecimal em dados binários. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>Parâmetros

 _SZ_
  
> [in] Ponteiro para a cadeia de ASCII terminada em nulo a ser convertido. Não é uma cadeia de caracteres Unicode. Caracteres válidos incluem os caracteres hexadecimais zero através de tanto quanto nove caracteres maiusculos e minúsculos A até F.
    
 _pb_
  
> [out] Ponteiro para o número binário retornado.
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> A cadeia de caracteres com êxito foi convertida em um número binário. 
    
FALSO 
  
> A cadeia de caracteres de entrada contém caracteres inválidos de hexadecimais ASCII.
    
## <a name="see-also"></a>Confira também



[ScBinFromHexBounded](scbinfromhexbounded.md)

