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
ms.openlocfilehash: e303361f4f0dd3a08dbb362096d07b8b391a6d97
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594415"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Localiza um equivalente do caminho local para o determinado caminho universal naming convention (UNC). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a>Parâmetros

 _szUNC_
  
> [in] Um caminho no formato \\[ _servidor_]\[ _compartilhar_]\[ _caminho_] de um arquivo ou diretório.
    
 _szLocal_
  
> [out] Um caminho no formato [ _unidade:_]\[ _caminho_] do arquivo ou diretório para o parâmetro _szUNC_ da mesma. 
    
 _cchLocal_
  
> [in] Tamanho do buffer da cadeia de caracteres de saída.
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> Um caminho local foi localizado com êxito.
    
MAPI_E_TOO_BIG
  
>  _szLocal_ não era grande o suficiente para armazenar o resultado. 
    
S_FALSE
  
> A cadeia de caracteres UNC já era um caminho local.
    
E_NOT_FOUND
  
> Um caminho local não foi encontrado.
    
## <a name="see-also"></a>Confira também



[ScUNCFromLocalPath](scuncfromlocalpath.md)

