---
title: ScUNCFromLocalPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScUNCFromLocalPath
api_type:
- COM
ms.assetid: cc4abf1a-c08c-4462-9d7c-6af506dc07c9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b53dd9aaaf18dba5c7e33e0bc7d984de757634a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414533"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Localiza uma contraparte de caminho de convenção universal de nomenclatura (UNC) para o caminho local fornecido.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a>Parâmetros

 _szLocal_
  
> no Um caminho no formato [ _unidade:_]\[ _caminho_] de um arquivo ou diretório.
    
 _szUNC_
  
> bota \\Um caminho no formato [ _Server_]\[ _share_]\[ _caminho_] do mesmo arquivo ou diretório que o parâmetro _szLocal_ . 
    
 _cchUNC_
  
> no Tamanho do buffer para a cadeia de caracteres de saída.
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> O equivalente ao caminho UNC foi localizado com êxito.
    
MAPI_E_INVALID_PARAMETER
  
> Um ou mais parâmetros são inválidos.
    
MAPI_E_TOO_BIG
  
>  _szUNC_ não era grande o suficiente para armazenar o resultado. 
    
S_FALSE
  
> O caminho local já era uma cadeia de caracteres UNC.
    
## <a name="see-also"></a>Confira também



[ScLocalPathFromUNC](sclocalpathfromunc.md)

