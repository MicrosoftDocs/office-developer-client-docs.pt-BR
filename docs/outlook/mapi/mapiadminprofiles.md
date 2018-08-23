---
title: MAPIAdminProfiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 843eed06f30dcca530cf4306c9e03bbffbb05af5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581283"
---
# <a name="mapiadminprofiles"></a>MAPIAdminProfiles

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um objeto de administração do perfil. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Bitmask dos sinalizadores indicando opções para a função de entrada de serviço. 
    
 _lppProfAdmin_
  
> [out] Ponteiro para um ponteiro para o novo objeto de administração do perfil.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetProfAdmin  <br/> |MFCMAPI usa o método **MAPIAdminProfiles** para obter o objeto de administração do perfil.  <br/> |
   
## <a name="see-also"></a>Confira também



[IProfAdmin::CreateProfile](iprofadmin-createprofile.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

