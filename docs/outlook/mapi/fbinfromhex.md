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
ms.openlocfilehash: 55c7deec9d29ae22a07b2f5ccd1c832d56782c03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341640"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Converte uma representação de cadeia de caracteres de um número hexadecimal em dados binários. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>Parâmetros

 _v_
  
> no Ponteiro para a cadeia de caracteres ASCII terminada em nulo para conversão. Não é uma cadeia de caracteres Unicode. Os caracteres válidos incluem os caracteres hexadecimais de zero a nove e os caracteres maiúsculos e minúsculos de A a F.
    
 _pb_
  
> bota Ponteiro para o número binário retornado.
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> A cadeia de caracteres foi convertida com êxito em um número binário. 
    
FALSE 
  
> A cadeia de caracteres de entrada contém caracteres hexadecimais ASCII inválidos.
    
## <a name="see-also"></a>Confira também



[ScBinFromHexBounded](scbinfromhexbounded.md)

