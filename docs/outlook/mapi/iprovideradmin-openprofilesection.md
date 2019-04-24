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
ms.openlocfilehash: b3ac1b2cf8335c5e0953fdcf61b2b5d466fbb724
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301544"
---
# <a name="iprovideradminopenprofilesection"></a>IProviderAdmin::OpenProfileSection

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma seção de perfil do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para obter mais acesso. 
  
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
  
> no Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo da seção de perfil a ser aberta. Os clientes não devem passar NULL para o parâmetro _lpUID_ . Os provedores de serviços podem passar NULL para recuperar o **MAPIUID** quando chamam de suas funções de ponto de entrada de serviço de mensagens. 
    
 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a seção de perfil. Passar resultados nulos na interface padrão da seção de perfil (**IProfSect**) que está sendo retornada. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como a seção de perfil é aberta. Os seguintes sinalizadores podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que o **OpenProfileSection** seja retornado com êxito, possivelmente antes que a seção de perfil esteja totalmente disponível para o chamador. Se a seção de perfil não estiver disponível, fazer uma chamada subsequente para ela poderá gerar um erro. 
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os objetos são abertos com permissão somente leitura, e os chamadores não devem funcionar na pressuposição de que a permissão de leitura/gravação tenha sido concedida. Os clientes não têm permissão de leitura/gravação para seções de provedor do perfil.
    
MAPI_FORCE_ACCESS
  
> Permite o acesso a todas as seções de perfil, mesmo aquelas pertencentes a provedores de serviços individuais.
    
 _lppProfSect_
  
> bota Um ponteiro para um ponteiro para a seção de perfil.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A seção de perfil foi aberta com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de modificar uma seção de perfil somente leitura ou para acessar um objeto para o qual o usuário tem permissões insuficientes.
    
MAPI_E_NOT_FOUND 
  
> A seção de perfil solicitada não existe.
    
## <a name="remarks"></a>Comentários

O método **IProviderAdmin:: OpenProfileSection** abre uma seção de perfil, permitindo que o chamador Leia informações e, possivelmente, grave informações no perfil ativo. 
  
Os clientes não podem abrir seções de perfil que pertencem a provedores usando o método **OpenProfileSection** . 
  
Vários clientes ou provedores de serviço podem abrir simultaneamente uma seção de perfil com permissão somente leitura. No enTanto, quando uma seção de perfil é aberta com permissão de leitura/gravação, nenhuma outra chamada pode ser feita para abrir a seção, independentemente do tipo de acesso. Se uma seção de perfil estiver aberta com permissão somente leitura, uma chamada subsequente para solicitar permissão de leitura/gravação falhará com o MAPI_E_NO_ACCESS. Da mesma forma, se uma seção estiver aberta com permissão de leitura/gravação, uma chamada subsequente para solicitar permissão somente leitura também falhará. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se você solicitar que **OpenProfileSection** abra uma seção de perfil não existente passando MAPI_MODIFY no _Parâmetroulflags_ e um **MAPIUID** desconhecido no _lpUID_, a seção de perfil será criada. 
  
Se você solicitar que **OpenProfileSection** abra uma seção não existente com permissão somente leitura, ele retornará MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIProfileFunctions. cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI usa o método **IProviderAdmin:: OpenProfileSection** para abrir uma seção de perfil do perfil atual.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

