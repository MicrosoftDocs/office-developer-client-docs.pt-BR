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
ms.openlocfilehash: e5043a614ccd94994fe86838f15aa1a43f22733e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412349"
---
# <a name="mapiadminprofiles"></a>MAPIAdminProfiles

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um objeto de administração de perfil. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Bitmask de sinalizadores que indicam opções para a função de entrada de serviço. 
    
 _lppProfAdmin_
  
> bota Ponteiro para um ponteiro para o novo objeto de administração de perfil.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIObjects. cpp  <br/> |CMapiObjects:: GetProfAdmin  <br/> |MFCMAPI usa o método **MAPIAdminProfiles** para obter o objeto de administração de perfil.  <br/> |
   
## <a name="see-also"></a>Confira também



[IProfAdmin::CreateProfile](iprofadmin-createprofile.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

