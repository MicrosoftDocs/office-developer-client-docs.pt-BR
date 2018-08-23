---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 135db8d690d4d4bd610bd15893c358fedddb4605
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589277"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Converte a parte especificada de uma representação de cadeia de caracteres de um número hexadecimal em um número binário. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>Parâmetros

 _SZ_
  
> [in] Ponteiro para a cadeia de caracteres terminada em nulo a ser convertido. Caracteres válidos incluem os caracteres hexadecimais 0 a 9 e os dois caracteres maiusculos e minúsculos a até f.
    
 _pb_
  
> [out] Ponteiro para o número binário retornado.
    
 _cb_
  
> [in] Tamanho, em bytes, do parâmetro _pb_ . 
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> Conversão foi bem sucedida.
    
MAPI_E_CALL_FAILED
  
> Caracteres inválidos encontrados.
    
## <a name="see-also"></a>Confira também



[FBinFromHex](fbinfromhex.md)

