---
title: Verificando a configuração de provedor de serviço
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f6190b2860e227b24b34e31a4ee9741468383460
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589634"
---
# <a name="verifying-service-provider-configuration"></a>Verificando a configuração de provedor de serviço
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Seu método de logon ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)ou [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) Verifique a configuração do seu provedor. Isso envolve a verificação de que todas as propriedades necessárias para a operação completa estão definidas corretamente. Cada provedor requer um número diferente de propriedades; configuração depende do seu provedor e o grau de você permitir a interação do usuário. Alguns provedores de serviços mantenha todas as propriedades necessárias no perfil. 

Outros provedores de serviços mantenha um conjunto parcial das propriedades no perfil e solicitar ao usuário de valores ausentes. Ainda outros provedores não armazene propriedades no perfil nisso, depender fornecer todas as informações necessárias para configuração do usuário.
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a>Para recuperar as propriedades armazenadas no perfil
  
1. Chame [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passando o [MAPIUID](mapiuid.md) do provedor de como um parâmetro de entrada. 
    
2. Chame métodos de [IMAPIProp::GetProps](imapiprop-getprops.md) ou [IMAPIProp::GetPropList](imapiprop-getproplist.md) da seção perfil para recuperar as propriedades individuais ou uma lista de propriedades. 
    
### <a name="to-set-properties-from-user-information"></a>Para definir as propriedades das informações do usuário
  
Exiba uma folha de propriedades, se MAPI não tiver definido um sinalizador proibindo a exibição. Sinalizadores a seguir indicam que uma interface de usuário não pode ser apresentada.
  
|**Flag**|**Provedor de serviços**|
|:-----|:-----|
|AB_NO_DIALOG  <br/> |Provedor de catálogo de endereços  <br/> |
|LOGON_NO_DIALOG  <br/> |Provedor de transporte  <br/> |
|MDB_NO_DIALOG  <br/> |Provedor de armazenamento de mensagem  <br/> |
   
Se seu provedor não armazena todas as suas propriedades de configuração do perfil, exigir interação do usuário e MAPI passa uma dos sinalizadores de supressão de caixa de diálogo para seu método de logon, retorne MAPI_E_UNCONFIGURED. Também retorne esse erro quando o sinalizador de supressão de diálogo não estiver definido, mas o usuário não fornecer todas as informações necessárias.
  
Quando seu provedor de serviço falha seu método de logon com MAPI_E_UNCONFIGURED, MAPI chama a função do ponto de entrada novamente. Se as informações não podem ser localizadas com a segunda chamada, talvez encerrar a sessão, dependendo de qual seu provedor de serviços é a importância. 
  
A ilustração a seguir mostra a lógica obrigatório para a configuração no seu método de logon do provedor de serviço. 
  
**Configuration verification flowchart**
  
![Fluxograma de verificação de configuração] (media/amapi_62.gif "Fluxograma de verificação de configuração")
  
## <a name="see-also"></a>Confira também

- [Implementar o logon do provedor de serviços](implementing-service-provider-logon.md)

