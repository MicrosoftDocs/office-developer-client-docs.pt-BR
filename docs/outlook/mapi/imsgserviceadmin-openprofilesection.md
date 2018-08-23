---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8dfa777480af48819e5357fad9b1e7524148a8b7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568809"
---
# <a name="imsgserviceadminopenprofilesection"></a>IMsgServiceAdmin::OpenProfileSection

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma seção do perfil atual e retorna um ponteiro de [IProfSect](iprofsectimapiprop.md) para obter mais acesso. 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a>Parâmetros

 _lpUID_
  
> Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que identifica a seção de perfil. 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar a seção de perfil. Passagem nula resulta em um ponteiro para sua interface padrão que está sendo retornada no parâmetro _lppProfSect_ . A interface padrão para uma seção de perfil é **IProfSect**.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o acesso à seção de perfil. Sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenProfileSection** retornar com êxito, possivelmente antes que o perfil seção é totalmente disponível para o cliente da chamada. Se o perfil da seção não estiver disponível, fazendo uma chamada subsequente a ele pode gerar um erro. 
    
MAPI_MODIFY 
  
> Permissão de leitura/gravação solicitações. Por padrão, seções de perfil são abertas com permissão somente leitura e os clientes não devem funcionar no pressuposto de que você recebeu permissão de leitura/gravação. 
    
MAPI_FORCE_ACCESS
  
> Permite o acesso a todas as seções de perfil, mesmo aqueles pertencentes a provedores de serviços individuais.
    
 _lppProfSect_
  
> [out] Um ponteiro para um ponteiro para a seção de perfil.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Seção perfil tiver sido aberta com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar uma seção de perfil para o qual o chamador tem permissões insuficientes.
    
E_NOT_FOUND 
  
> A seção de perfil solicitada não existe.
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin::OpenProfileSection** abre uma seção de perfil, um objeto que dá suporte à interface [IProfSect](iprofsectimapiprop.md) . As seções de perfil são usadas para ler informações do e gravando informações do perfil da sessão. 
  
 **OpenProfileSection** não pode ser usado para abrir seções perfil pertencentes a provedores de serviços individuais, a menos que MAPI_FORCE_ACCESS é usado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Vários clientes podem abrir uma seção de perfil com permissão somente leitura, mas apenas um cliente pode abrir uma seção de perfil com permissão de leitura/gravação. Se outro cliente tiver uma seção de perfil abra se você tenta abrir chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY definido, a chamada irá falhar, retornando MAPI_E_NO_ACCESS. 
  
Uma operação de abertura somente leitura falhará se a seção está aberta para gravação. 
  
Você pode criar uma seção de perfil chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY e uma estrutura [MAPIUID](mapiuid.md) inexistente no parâmetro _lpUID_ . Certifique-se de que você especificar MAPI_MODIFY. Se você definir _lpUID_ para apontar para um inexistente **MAPIUID** e **OpenProfileSection** está definido para usar o modo de padrão de acesso de somente leitura, a chamada irá falhar com MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI usa o método **IMsgServiceAdmin::OpenProfileSection** para abrir uma seção de perfil.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

