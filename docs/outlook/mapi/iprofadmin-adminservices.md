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
ms.openlocfilehash: a9e596ff8561d5aabc71ffe3540efaeef8f5b83d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593981"
---
# <a name="iprofadminadminservices"></a>IProfAdmin::AdminServices

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso a um objeto de administração do serviço de mensagem para aplicar alterações para os serviços de mensagem em um perfil.
  
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
  
> [in] Um ponteiro para o nome do perfil a ser modificada. O parâmetro _lpszProfileName_ não deve ser NULL. 
    
 _lpszPassword_
  
> [in] Sempre nulo. 
    
 _ulUIParam_
  
> [in] Uma alça da janela pai para todas as caixas de diálogo ou windows que esse método exibe.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla a recuperação do objeto de administração do serviço de mensagem. Sinalizadores a seguir podem ser definidos:
    
MAPI_DIALOG 
  
> Habilita a exibição de uma interface de usuário. 
    
MAPI_UNICODE 
  
> O nome do perfil está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o nome é no formato ANSI.
    
 _lppServiceAdmin_
  
> [out] Um ponteiro para um ponteiro para um objeto de administração do serviço de mensagem.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O objeto de administração do serviço de mensagem foi retornado com êxito.
    
MAPI_E_LOGON_FAILED 
  
> O perfil especificado não existe, ou a senha estava errada e uma caixa de diálogo não pôde ser exibida ao usuário para solicitar a senha correta porque MAPI_DIALOG não foi definido em _ulFlags_.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O método **IProfAdmin::AdminServices** fornece acesso a um objeto de administração do serviço de mensagem para as alterações de configuração a mensagem serviços em um perfil. 
  
 O parâmetro _lpszPassword_ deve ser NULL ou um ponteiro para uma cadeia de caracteres de comprimento zero. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Embora você possa recuperar um ponteiro [IMsgServiceAdmin](imsgserviceadminiunknown.md) chamando este método ou o [IMAPISession::AdminServices](imapisession-adminservices.md), chame **IProfAdmin::AdminServices** se você tiver estritamente um cliente de configuração e oferece sem recursos de mensagens. **IProfAdmin::AdminServices** não cria um objeto de sessão e não carregar quaisquer provedores de serviço, que melhora o desempenho. 
  
Você não pode usar **IProfAdmin::AdminServices** para criar um perfil. Portanto, você deve especificar um perfil de válido existente no _lpszProfileName_. Se o perfil especificado não existir, o **IProfAdmin::AdminServices** retornará MAPI_E_LOGON_FAILED. 
  
O nome do perfil pode ter até 64 caracteres de comprimento e pode incluir os seguintes caracteres:
  
- Todos os caracteres alfanuméricos, incluindo o caractere de sublinhado e ênfase. 
    
- Espaços incorporados, mas não espaços à esquerda ou à direita.
    
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> | HrAddServiceToProfile  <br/> |MFCMAPI usa o método **IProfAdmin::AdminServices** para abrir um objeto de administração do serviço de mensagem para o perfil selecionado adicionar serviços.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

