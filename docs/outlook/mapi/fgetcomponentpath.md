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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384497"
---
# <a name="fgetcomponentpath"></a>FGetComponentPath

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o caminho para o Mapi32 privada.
  
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
  
> [in] A chave do registro MSIComponentID descrito nas [Configurações de registro de Stub Mapi32](https://msdn.microsoft.com/library/dd162409.aspx).
    
 _szQualifier_
  
> [in] A subchave MSIApplicationLCID ou MSIOfficeLCID descrita na [Escolha de uma versão específica de MAPI a carga](how-to-choose-a-specific-version-of-mapi-to-load.md). Os chamadores podem passar **null** se não houver nenhum qualificador. 
    
 _szDllPath_
  
> [in] O caminho para o Mapi32 privada, que tem a funcionalidade total do MAPI (as exportações mesmas como o Mapi32).
    
 _cchBufferSize_
  
> [in] O tamanho da _szDllPath_, em caracteres.
    
 _fInstall_
  
> [in] Informa MAPI para instalar o componente de Mapi32 privado se ele está ausente.
    
## <a name="return-value"></a>Valor de retorno

 **True**
  
> O caminho foi encontrado.
    
 **False**
  
> O caminho não foi encontrado.
    
## <a name="remarks"></a>Comentários

Use a função de **FGetComponentPath** quando precisar fazer o caminho para o Mapi32 privada. 
  
## <a name="see-also"></a>Confira também



[Escolher uma versão específica de MAPI para carga](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Configurações de registro de Stub Mapi32](https://msdn.microsoft.com/library/dd162409.aspx)

