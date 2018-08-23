---
title: IProviderAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: b73cf770-8817-4a23-bd14-7b76fedef214
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0f917989d9bac403f2bea5b2d6699b7a1caf2008
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573009"
---
# <a name="iprovideradminopenprofilesection"></a>IProviderAdmin::OpenProfileSection

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma seção de perfil do perfil atual e retorna um ponteiro de [IProfSect](iprofsectimapiprop.md) para obter mais acesso. 
  
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
  
> [in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo para a seção de perfil para ser aberto. Os clientes não precisam passar NULL para o parâmetro _lpUID_ . Provedores de serviços podem passar NULL para recuperar o **MAPIUID** quando ele liga de suas funções de ponto de entrada de serviço de mensagem. 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar a seção de perfil. Passagem nula resulta na interface para padrão da seção perfil (**IProfSect**) que está sendo retornado. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a seção de perfil é aberta. Sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **OpenProfileSection** retornar com êxito, possivelmente antes da seção de perfil é totalmente disponível para o chamador. Se o perfil da seção não estiver disponível, fazendo uma chamada subsequente a ele pode gerar um erro. 
    
MAPI_MODIFY 
  
> Permissão de leitura/gravação solicitações. Por padrão, os objetos são abertos com permissão somente leitura e os chamadores não devem funcionar no pressuposto de que você recebeu permissão de leitura/gravação. Os clientes não são permitidos a permissão de leitura/gravação às seções de provedor do perfil.
    
MAPI_FORCE_ACCESS
  
> Permite o acesso a todas as seções de perfil, mesmo aqueles pertencentes a provedores de serviços individuais.
    
 _lppProfSect_
  
> [out] Um ponteiro para um ponteiro para a seção de perfil.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Seção perfil tiver sido aberta com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa para modificar uma seção de perfil de somente leitura ou para acessar um objeto para o qual o usuário tem permissões insuficientes.
    
E_NOT_FOUND 
  
> A seção de perfil solicitada não existe.
    
## <a name="remarks"></a>Comentários

O método **IProviderAdmin::OpenProfileSection** abre uma seção de perfil, permitindo que o chamador ler informações de e possivelmente gravar informações sobre o perfil ativo. 
  
Os clientes não podem abrir seções de perfil que pertencem a provedores usando o método **OpenProfileSection** . 
  
Vários clientes ou provedores de serviços simultaneamente podem abrir uma seção de perfil com permissão somente leitura. No entanto, quando uma seção de perfil é aberta com permissão de leitura/gravação, nenhuma outra chamada pode ser feita para abrir a seção, independentemente do tipo de acesso. Se uma seção de perfil estiver aberta com permissão somente leitura, uma chamada subsequente para solicitar a permissão de leitura/gravação falhará com MAPI_E_NO_ACCESS. Da mesma forma, se uma seção estiver aberta com permissão de leitura/gravação, uma chamada subsequente para solicitar permissão somente leitura também falhará. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se você solicitar que **OpenProfileSection** abrir uma seção de perfil inexistente, passando MAPI_MODIFY em _ulFlags_ e um desconhecido **MAPIUID** em _lpUID_, a seção de perfil será criado. 
  
Se você solicitar que **OpenProfileSection** abrir uma seção inexistente com permissão somente leitura, ele retornará E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI usa o método **IProviderAdmin::OpenProfileSection** para abrir uma seção de perfil do perfil atual.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

