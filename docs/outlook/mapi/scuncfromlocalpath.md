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
ms.openlocfilehash: faba91d813d27f7ea45e978724ce0d4707803cba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590103"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Localiza um equivalente universal de nomenclatura do caminho UNC (convenção) para o caminho local fornecido.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a>Parâmetros

 _szLocal_
  
> [in] Um caminho no formato [ _unidade:_]\[ _caminho_] de um arquivo ou diretório.
    
 _szUNC_
  
> [out] Um caminho no formato \\[ _servidor_]\[ _compartilhar_]\[ _caminho_] do arquivo ou diretório para o parâmetro _szLocal_ da mesma. 
    
 _cchUNC_
  
> [in] Tamanho do buffer da cadeia de caracteres de saída.
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> O equivalente do caminho UNC foi localizado com êxito.
    
MAPI_E_INVALID_PARAMETER
  
> Um ou mais parâmetros são inválidos.
    
MAPI_E_TOO_BIG
  
>  _szUNC_ não era grande o suficiente para armazenar o resultado. 
    
S_FALSE
  
> O caminho local já foi uma cadeia de caracteres UNC.
    
## <a name="see-also"></a>Confira também



[ScLocalPathFromUNC](sclocalpathfromunc.md)

