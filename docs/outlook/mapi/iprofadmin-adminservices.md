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
  
Fornece acesso a um objeto de administração de serviço de mensagens para fazer alterações nos serviços de mensagens em um perfil.
  
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
  
> no Um ponteiro para o nome do perfil a ser modificado. O parâmetro _lpszProfileName_ não deve ser nulo. 
    
 _lpszPassword_
  
> no Sempre nulo. 
    
 _ulUIParam_
  
> no Um identificador da janela pai para quaisquer caixas de diálogo ou janelas que esse método exibe.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla a recuperação do objeto de administração do serviço de mensagens. Os seguintes sinalizadores podem ser definidos:
    
MAPI_DIALOG 
  
> Permite a exibição de uma interface do usuário. 
    
MAPI_UNICODE 
  
> O nome do perfil está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o nome estará no formato ANSI.
    
 _lppServiceAdmin_
  
> bota Um ponteiro para um ponteiro para um objeto de administração de serviço de mensagens.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O objeto de administração do serviço de mensagens foi retornado com êxito.
    
MAPI_E_LOGON_FAILED 
  
> O perfil especificado não existe ou a senha estava errada e uma caixa de diálogo não pôde ser exibida para o usuário solicitar a senha correta porque o MAPI_DIALOG não foi definido no _parâmetroulflags_.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O método **IProfAdmin:: adminservices** fornece acesso a um objeto de administração do serviço de mensagens para fazer alterações de configuração nos serviços de mensagens em um perfil. 
  
 O parâmetro _lpszPassword_ deve ser NULL ou um ponteiro para uma sequência de comprimento zero. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Embora você possa recuperar um ponteiro do [IMsgServiceAdmin](imsgserviceadminiunknown.md) chamando esse método ou [IMAPISession:: adminservices](imapisession-adminservices.md), Call **IProfAdmin:: adminservices** se você tiver estritamente um cliente de configuração e não oferecer recursos de mensagens. **IProfAdmin:: adminservices** não cria um objeto Session e não carrega nenhum provedor de serviços, o que melhora o desempenho. 
  
Você não pode usar **IProfAdmin:: admins** para criar um perfil. Portanto, você deve especificar um perfil válido existente no _lpszProfileName_. Se o perfil especificado não existir, **IProfAdmin:: adminservices** retornará MAPI_E_LOGON_FAILED. 
  
O nome do perfil pode ter até 64 caracteres de comprimento e pode incluir os seguintes caracteres:
  
- Todos os caracteres alfanuméricos, incluindo caracteres de ênfase e o caractere de sublinhado. 
    
- Espaços incorporados, mas não espaços à esquerda ou à direita.
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIProfileFunctions. cpp  <br/> | HrAddServiceToProfile  <br/> |MFCMAPI usa o método **IProfAdmin:: adminservices** para abrir um objeto de administração de serviço de mensagens para o perfil selecionado para adicionar serviços.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

