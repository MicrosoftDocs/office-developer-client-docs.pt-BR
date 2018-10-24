---
title: Criar um perfil usando um código personalizado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c14d58e8a03633615798b50b256b9cc54fcc4f4c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594730"
---
# <a name="creating-a-profile-by-using-custom-code"></a>Criar um perfil usando um código personalizado

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se você optar por escrever código para criar um perfil, certifique-se de que entendeu como entradas de perfil e o tipo e a quantidade de informações que é necessária para cada entrada de pedidos. As implicações de ordenação entradas em um perfil é explicada com [Perfis MAPI](mapi-profiles.md).
  
 **Para criar um perfil com código C ou C++**
  
1. Leia o arquivo de cabeçalho para cada serviço de mensagem. Compreender as propriedades que você precisará configurar e quais valores que você usará.
    
2. Chame a função [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar um ponteiro de interface **IProfAdmin** . 
    
3. Chame [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) para criar seu perfil. Se você deseja criar um perfil com a mensagem serviços listados na seção **[Padrão Services]** do MAPISVC. Arquivo INF, defina o sinalizador MAPI_DEFAULT_SERVICE. Se você quiser permitir que o usuário digitar as informações de configuração, defina o sinalizador MAPI_DIALOG. Certifique-se de que você definir esse sinalizador se não todas as informações necessárias está disponível por meio do MAPISVC. Arquivo INF. **CreateProfile** chama a função do ponto de entrada para cada serviço de mensagem a ser adicionada ao perfil com MSG_SERVICE_CREATE definido como o parâmetro _ulContext_ . 
    
4. Chame [IProfAdmin::AdminServices](iprofadmin-adminservices.md) para obter um objeto de administração do serviço de mensagem. 
    
5. Use o objeto de administração do serviço de mensagem para adicionar serviços de mensagens ao perfil. Para cada serviço de mensagem que você deseja adicionar:
    
1. Chame o método [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) para criar o novo serviço de mensagem. 
    
2. Chame [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passando a estrutura **MAPIUID** do serviço que você acabou de criar e uma matriz de valores de propriedade com suas propriedades de configuração. 
    
6. Para recuperar o identificador de um serviço recém-adicionado, que é sua propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)), chame [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para acessar a tabela de serviços de mensagem e pesquisa para a linha que representa o serviço de mensagem. A última linha da tabela representará o serviço de mensagem adicionado mais recentemente. 
    
Para tornar um novo perfil temporário, chame o método de [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) imediatamente após o logon. **DeleteProfile** marcará o novo perfil como excluído, tornando pode ser usado para a duração da sessão. Porque ele não será incluído na tabela de perfil da sessão, outros clientes poderão usá-lo. 
  

