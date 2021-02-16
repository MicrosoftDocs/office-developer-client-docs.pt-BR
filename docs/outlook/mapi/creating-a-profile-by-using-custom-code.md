---
title: Criando um perfil usando código personalizado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f3270528194b3cc3429d3afec153355349dabbff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413301"
---
# <a name="creating-a-profile-by-using-custom-code"></a>Criando um perfil usando código personalizado

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se você optar por escrever código para criar um perfil, certifique-se de entender como ordenar entradas de perfil e o tipo e a quantidade de informações necessárias para cada entrada. As implicações da ordenação de entradas em um perfil são explicadas em [perfis MAPI.](mapi-profiles.md)
  
 **Para criar um perfil com código C ou C++**
  
1. Leia o arquivo de header para cada serviço de mensagens. Entenda quais propriedades você precisará configurar e quais valores serão usados.
    
2. Chame a [função MAPIAdminProfiles](mapiadminprofiles.md) para recuperar um ponteiro da interface **IProfAdmin.** 
    
3. Chame [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) para criar seu perfil. Se você quiser criar um perfil com os serviços de mensagem listados na seção **[Serviços Padrão]** do MAPISVC. Arquivo INF, de definida a MAPI_DEFAULT_SERVICE sinalizador. Se você deseja habilitar o usuário para inserir informações de configuração, de definida a MAPI_DIALOG sinalizador. Certifique-se de definir esse sinalizador se nem todas as informações necessárias estão disponíveis por meio do MAPISVC. Arquivo INF. **CreateProfile** chama a função de ponto de entrada para cada serviço de mensagem a ser adicionado ao perfil com MSG_SERVICE_CREATE definido como _o parâmetro ulContext._ 
    
4. Chame [IProfAdmin::AdminServices](iprofadmin-adminservices.md) para obter um objeto de administração do serviço de mensagens. 
    
5. Use o objeto de administração do serviço de mensagens para adicionar serviços de mensagem ao perfil. Para cada serviço de mensagens que você deseja adicionar:
    
1. Chame o [método IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) para criar o novo serviço de mensagens. 
    
2. Chame [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passando a estrutura **MAPIUID** do serviço que você acabou de criar e uma matriz de valores de propriedade com suas propriedades de configuração. 
    
6. Para recuperar o identificador de um serviço recém-adicionado, que é sua propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)), chame [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para acessar a tabela de serviço de mensagens e pesquise a linha que representa o serviço de mensagem. A última linha na tabela representará o serviço de mensagens adicionado mais recentemente. 
    
Para tornar um novo perfil temporário, chame o [método IProfAdmin::D eleteProfile](iprofadmin-deleteprofile.md) imediatamente depois de fazer logon. **DeleteProfile** marcará o novo perfil como excluído, tornando-o acessível durante a sessão. Como ele não será incluído na tabela de perfil da sessão, outros clientes não poderão usá-la. 
  

