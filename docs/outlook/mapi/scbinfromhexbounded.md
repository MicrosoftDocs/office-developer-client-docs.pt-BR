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
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439755"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Converte a parte especificada de uma representação de cadeia de caracteres de um número hexadecimal em um número binário. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>Parâmetros

 _v_
  
> no Ponteiro para a cadeia de caracteres terminada em nulo a ser convertido. Os caracteres válidos incluem os caracteres hexadecimais de 0 a 9 e os caracteres maiúsculos e minúsculos de a a f.
    
 _pb_
  
> bota Ponteiro para o número binário retornado.
    
 _cb_
  
> no Tamanho, em bytes, do parâmetro _PB_ . 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A conversão foi bem-sucedida.
    
MAPI_E_CALL_FAILED
  
> Foram encontrados caracteres inVálidos.
    
## <a name="see-also"></a>Confira também



[FBinFromHex](fbinfromhex.md)

