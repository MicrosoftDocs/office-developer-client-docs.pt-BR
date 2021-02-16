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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405657"
---
# <a name="iprovideradminopenprofilesection"></a>IProviderAdmin::OpenProfileSection

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma seção de perfil do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para mais acesso. 
  
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
  
> [in] Um ponteiro para a [estrutura MAPIUID](mapiuid.md) que contém o identificador exclusivo da seção de perfil a ser aberta. Os clientes não devem passar NULL para _o parâmetro lpUID._ Os provedores de serviços podem passar NULL para recuperar **o MAPIUID** quando ligarem de suas funções de ponto de entrada do serviço de mensagens. 
    
 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar a seção de perfil. Passar resultados NULL na interface padrão da seção de perfil (**IProfSect**) sendo retornado. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como a seção de perfil é aberta. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenProfileSection** retorne com êxito, possivelmente antes que a seção de perfil seja totalmente disponível para o chamador. Se a seção de perfil não estiver disponível, fazer uma chamada subsequente pode criar um erro. 
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os objetos são abertos com permissão somente leitura e os chamadores não devem trabalhar com a suposição de que a permissão de leitura/gravação foi concedida. Os clientes não têm permissão de leitura/gravação nas seções do provedor do perfil.
    
MAPI_FORCE_ACCESS
  
> Permite o acesso a todas as seções de perfil, mesmo aquelas pertencentes a provedores de serviços individuais.
    
 _lppProfSect_
  
> [out] Um ponteiro para um ponteiro para a seção de perfil.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A seção de perfil foi aberta com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de modificar uma seção de perfil somente leitura ou acessar um objeto para o qual o usuário tem permissões insuficientes.
    
MAPI_E_NOT_FOUND 
  
> A seção de perfil solicitada não existe.
    
## <a name="remarks"></a>Comentários

O **método IProviderAdmin::OpenProfileSection** abre uma seção de perfil, permitindo que o chamador leia informações e possivelmente escreva informações no perfil ativo. 
  
Os clientes não podem abrir seções de perfil que pertencem a provedores usando **o método OpenProfileSection.** 
  
Vários clientes ou provedores de serviços podem abrir simultaneamente uma seção de perfil com permissão somente leitura. No entanto, quando uma seção de perfil é aberta com permissão de leitura/gravação, nenhuma outra chamada pode ser feita para abrir a seção, independentemente do tipo de acesso. Se uma seção de perfil estiver aberta com permissão somente leitura, uma chamada subsequente para solicitar permissão de leitura/gravação falhará com MAPI_E_NO_ACCESS. Da mesma forma, se uma seção estiver aberta com permissão de leitura/gravação, uma chamada subsequente para solicitar permissão somente leitura também falhará. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se você solicitar que **OpenProfileSection** abra uma seção de perfil inexistente passando MAPI_MODIFY em  _ulFlags_ e um **MAPIUID** desconhecido em  _lpUID_, a seção de perfil será criada. 
  
Se você solicitar que **OpenProfileSection** abra uma seção inexistente com permissão somente leitura, ela retornará MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI usa o **método IProviderAdmin::OpenProfileSection** para abrir uma seção de perfil do perfil atual.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

