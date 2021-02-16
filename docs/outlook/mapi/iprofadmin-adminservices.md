---
title: IProfAdminAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.AdminServices
api_type:
- COM
ms.assetid: 87235fd2-6527-41a1-98ba-b951632a1c81
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2c504f98655e35af62810dd428e8e04878a36dec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422079"
---
# <a name="iprofadminadminservices"></a>IProfAdmin::AdminServices

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso a um objeto de administração do serviço de mensagens para fazer alterações nos serviços de mensagem em um perfil.
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>Parâmetros

 _lpszProfileName_
  
> [in] Um ponteiro para o nome do perfil a ser modificado. O  _parâmetro lpszProfileName_ não deve ser NULL. 
    
 _lpszPassword_
  
> [in] Sempre NULO. 
    
 _ulUIParam_
  
> [in] Um alça da janela pai para quaisquer caixas de diálogo ou janelas que esse método exibe.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla a recuperação do objeto de administração do serviço de mensagens. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DIALOG 
  
> Habilita a exibição de uma interface do usuário. 
    
MAPI_UNICODE 
  
> O nome do perfil está no formato Unicode. Se o MAPI_UNICODE sinalizador não estiver definido, o nome está no formato ANSI.
    
 _lppServiceAdmin_
  
> [out] Um ponteiro para um ponteiro para um objeto de administração do serviço de mensagens.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O objeto de administração do serviço de mensagens foi retornado com êxito.
    
MAPI_E_LOGON_FAILED 
  
> O perfil especificado não existe ou a senha estava errada e não foi possível exibir uma caixa de diálogo para o usuário solicitar a senha correta porque MAPI_DIALOG não foi definido em _ulFlags._
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, normalmente clicando no botão Cancelar **em** uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O **método IProfAdmin::AdminServices** fornece acesso a um objeto de administração do serviço de mensagens para fazer alterações de configuração nos serviços de mensagem em um perfil. 
  
 O  _parâmetro lpszPassword_ deve ser NULL ou um ponteiro para uma cadeia de caracteres de comprimento zero. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Embora você possa recuperar um ponteiro [IMsgServiceAdmin](imsgserviceadminiunknown.md) chamando esse método ou [IMAPISession::AdminServices](imapisession-adminservices.md), chame **IProfAdmin::AdminServices** se você tiver estritamente um cliente de configuração e não oferecer nenhum recurso de mensagens. **IProfAdmin::AdminServices** não cria um objeto de sessão e não carrega nenhum provedor de serviços, o que melhora o desempenho. 
  
Você não pode **usar IProfAdmin::AdminServices** para criar um perfil. Portanto, você deve especificar um perfil válido existente  _em lpszProfileName_. Se o perfil especificado não existir, **IProfAdmin::AdminServices** retornará MAPI_E_LOGON_FAILED. 
  
O nome do perfil pode ter até 64 caracteres e incluir os seguintes caracteres:
  
- Todos os caracteres alfanuméricos, incluindo caracteres de destaque e o caractere de sublinhado. 
    
- Espaços incorporados, mas não espaços à frente ou à frente.
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> | HrAddServiceToProfile  <br/> |MFCMAPI usa o **método IProfAdmin::AdminServices** para abrir um objeto de administração de serviço de mensagens para o perfil selecionado adicionar serviços.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

