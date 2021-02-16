---
title: ScLocalPathFromUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScLocalPathFromUNC
api_type:
- COM
ms.assetid: ef5eb5c6-251e-4a3a-8855-7c28804a29ab
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e7607a57da5b618a20d6c8e360c7e3cb4f933856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432230"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Localiza uma contraparte de caminho local para o caminho UNC (convenção de nomenu universal). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a>Parâmetros

 _szUNC_
  
> [in] Um caminho no formato \\ [ _servidor_] \[ _compartilhamento_] \[ _caminho_] de um arquivo ou diretório.
    
 _szLocal_
  
> [out] Um caminho no formato [ _unidade:_] caminho ] do mesmo arquivo ou \[ diretório como para o _parâmetro szUNC._ 
    
 _cchLocal_
  
> [in] Tamanho do buffer para a cadeia de caracteres de saída.
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> Um caminho local foi localizado com êxito.
    
MAPI_E_TOO_BIG
  
>  _szLocal_ não era grande o suficiente para conter o resultado. 
    
S_FALSE
  
> A cadeia de caracteres UNC já era um caminho local.
    
MAPI_E_NOT_FOUND
  
> Um caminho local não foi encontrado.
    
## <a name="see-also"></a>Confira também



[ScUNCFromLocalPath](scuncfromlocalpath.md)

