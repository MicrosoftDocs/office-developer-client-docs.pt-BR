---
title: FGetComponentPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FGetComponentPath
api_type:
- COM
ms.assetid: 2a303458-3283-409a-bc3b-b891f3fcfc22
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3456d81935a0a94bc2158eefd321da968dda9983
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335207"
---
# <a name="fgetcomponentpath"></a>FGetComponentPath

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o caminho para o campo Mapi32.dll.
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a>Parâmetros

 _szComponent_
  
> [in] A chave do registro MSIComponentID descrita emMapi32.dll do Registro [stub.](https://msdn.microsoft.com/library/dd162409.aspx)
    
 _szQualifier_
  
> [in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md). Os chamadores podem passar **nulo** se não houver qualificador. 
    
 _szDllPath_
  
> [in] O caminho para o Mapi32.dll privado, que tem funcionalidade MAPI completa (as mesmas exportações que o Mapi32.dll).
    
 _cchBufferSize_
  
> [in] O tamanho de  _szDllPath_, em caracteres.
    
 _fInstall_
  
> [in] Informa ao MAPI para instalar o componente Mapi32.dll privado se ele estiver ausente.
    
## <a name="return-value"></a>Valor de retorno

 **verdadeiro**
  
> O caminho foi encontrado.
    
 **falso**
  
> O caminho não foi encontrado.
    
## <a name="remarks"></a>Comentários

Use a **função FGetComponentPath** quando precisar obter o caminho para o grupo Mapi32.dll. 
  
## <a name="see-also"></a>Confira também



[Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Mapi32.dll do Registro stub](https://msdn.microsoft.com/library/dd162409.aspx)

