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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e4bce7f122522532023d18b43fe4bfdeda84af9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766537"
---
# <a name="fgetcomponentpath"></a>FGetComponentPath

  
  
**Aplica-se a**: Outlook 
  
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

## <a name="parameters"></a>Par�metros

 _szComponent_
  
> [in] A chave do registro MSIComponentID descrito nas [Configurações de registro de Stub Mapi32](http://msdn.microsoft.com/en-us/library/dd162409.aspx).
    
 _szQualifier_
  
> [in] A subchave MSIApplicationLCID ou MSIOfficeLCID descrita na [Escolha de uma versão específica de MAPI a carga](how-to-choose-a-specific-version-of-mapi-to-load.md). Os chamadores podem passar **null** se não houver nenhum qualificador. 
    
 _szDllPath_
  
> [in] O caminho para o Mapi32 privada, que tem a funcionalidade total do MAPI (as exportações mesmas como o Mapi32).
    
 _cchBufferSize_
  
> [in] O tamanho da _szDllPath_, em caracteres.
    
 _fInstall_
  
> [in] Informa MAPI para instalar o componente de Mapi32 privado se ele está ausente.
    
## <a name="return-value"></a>Valor retornado

 **True**
  
> O caminho foi encontrado.
    
 **False**
  
> O caminho não foi encontrado.
    
## <a name="remarks"></a>Coment�rios

Use a função de **FGetComponentPath** quando precisar fazer o caminho para o Mapi32 privada. 
  
## <a name="see-also"></a>Confira também



[Escolher uma versão específica de MAPI para carga](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Configurações de registro de Stub Mapi32](http://msdn.microsoft.com/en-us/library/dd162409.aspx)

