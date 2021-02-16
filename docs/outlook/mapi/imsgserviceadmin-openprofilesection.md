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
ms.openlocfilehash: 32ebdea3a594b5adf5d46dc081098d3628ae145b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437109"
---
# <a name="imsgserviceadminopenprofilesection"></a>IMsgServiceAdmin::OpenProfileSection

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma seção do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para mais acesso. 
  
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
  
> Um ponteiro para a [estrutura MAPIUID](mapiuid.md) que identifica a seção de perfil. 
    
 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar a seção de perfil. Passar NULL resulta em um ponteiro para sua interface padrão sendo retornada no _parâmetro lppProfSect._ A interface padrão para uma seção de perfil **é IProfSect**.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o acesso à seção de perfil. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenProfileSection** retorne com êxito, possivelmente antes que a seção de perfil seja totalmente disponível para o cliente de chamada. Se a seção de perfil não estiver disponível, fazer uma chamada subsequente pode criar um erro. 
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, as seções de perfil são abertas com permissão somente leitura, e os clientes não devem trabalhar com a suposição de que a permissão de leitura/gravação foi concedida. 
    
MAPI_FORCE_ACCESS
  
> Permite o acesso a todas as seções de perfil, mesmo aquelas pertencentes a provedores de serviços individuais.
    
 _lppProfSect_
  
> [out] Um ponteiro para um ponteiro para a seção de perfil.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A seção de perfil foi aberta com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar uma seção de perfil para a qual o chamador tem permissões insuficientes.
    
MAPI_E_NOT_FOUND 
  
> A seção de perfil solicitada não existe.
    
## <a name="remarks"></a>Comentários

O **método IMsgServiceAdmin::OpenProfileSection** abre uma seção de perfil, um objeto que oferece suporte à interface [IProfSect.](iprofsectimapiprop.md) As seções de perfil são usadas para ler informações e escrever informações no perfil da sessão. 
  
 **OpenProfileSection** não pode ser usado para abrir seções de perfil pertencentes a provedores de serviços individuais, a menos que MAPI_FORCE_ACCESS seja usado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Vários clientes podem abrir uma seção de perfil com permissão somente leitura, mas somente um cliente pode abrir uma seção de perfil com permissão de leitura/gravação. Se outro cliente tiver uma seção de perfil aberta que você tente abrir chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY definido, a chamada falhará, retornando MAPI_E_NO_ACCESS. 
  
Uma operação de abertura somente leitura falhará se a seção estiver aberta para escrita. 
  
Você pode criar uma seção de perfil chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY e uma estrutura [MAPIUID](mapiuid.md) inexistente no parâmetro _lpUID._ Certifique-se de especificar MAPI_MODIFY. Se você definir  _lpUID_ para apontar para um **MAPIUID** inexistente e **OpenProfileSection** for definido para usar o modo de acesso padrão de somente leitura, a chamada falhará com MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI usa o **método IMsgServiceAdmin::OpenProfileSection** para abrir uma seção de perfil.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

