---
title: Verificar a configuração do provedor de serviços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 381e2c9ec84811b69d666017a568e7b9cca21755
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418845"
---
# <a name="verifying-service-provider-configuration"></a>Verificar a configuração do provedor de serviços
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O método de logon ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)ou [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) deve verificar a configuração do provedor. Isso envolve a verificação de que todas as propriedades necessárias para a operação completa estão definidas corretamente. Cada provedor requer um número diferente de propriedades; depende do provedor e do grau de interação do usuário que você permite. Alguns provedores de serviços mantêm todas as propriedades necessárias no perfil. 

Outros provedores de serviços mantêm um conjunto parcial de propriedades no perfil e solicitam valores ausentes ao usuário. Ainda assim, outros provedores não armazenam propriedades no perfil, confiando no usuário para fornecer todas as informações necessárias para a configuração.
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a>Para recuperar propriedades armazenadas no perfil
  
1. Chame [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passando [o MAPIUID](mapiuid.md) do seu provedor como um parâmetro de entrada. 
    
2. Chame os métodos [IMAPIProp::GetProps](imapiprop-getprops.md) ou [IMAPIProp::GetPropList](imapiprop-getproplist.md) da seção de perfil para recuperar propriedades individuais ou uma lista de propriedades. 
    
### <a name="to-set-properties-from-user-information"></a>Para definir propriedades de informações do usuário
  
Exibir uma folha de propriedades, se MAPI não tiver definido um sinalizador proibindo a exibição. Os sinalizadores a seguir indicam que uma interface do usuário não pode ser apresentada.
  
|**Flag**|**Provedor de serviços**|
|:-----|:-----|
|AB_NO_DIALOG  <br/> |Provedor de agendas  <br/> |
|LOGON_NO_DIALOG  <br/> |Provedor de transporte  <br/> |
|MDB_NO_DIALOG  <br/> |Provedor de armazenamento de mensagens  <br/> |
   
Se o provedor não armazenar todas as suas propriedades de configuração no perfil, exigindo interação do usuário, e o MAPI passar um dos sinalizadores de supressão da caixa de diálogo para o método de logon, retorne MAPI_E_UNCONFIGURED. Também retornará esse erro quando o sinalizador de supressão de caixa de diálogo não estiver definido, mas o usuário não fornecerá todas as informações necessárias.
  
Quando o provedor de serviços falha no método de logon com MAPI_E_UNCONFIGURED, o MAPI chama sua função de ponto de entrada novamente. Se as informações não puderem ser localizadas com a segunda chamada, a sessão poderá ser encerrada, dependendo da importância do provedor de serviços. 
  
A ilustração a seguir mostra a lógica necessária para a configuração no método de logon do provedor de serviços. 
  
**Configuration verification flowchart**
  
![Fluxograma verificação de configuração](media/amapi_62.gif "Fluxograma verificação de configuração")
  
## <a name="see-also"></a>Confira também

- [Implementando o logon do provedor de serviços](implementing-service-provider-logon.md)

