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
ms.openlocfilehash: f3270528194b3cc3429d3afec153355349dabbff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413301"
---
# <a name="creating-a-profile-by-using-custom-code"></a>Criar um perfil usando um código personalizado

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se você optar por escrever código para criar um perfil, certifique-se de que você compreende como solicitar entradas de perfil e o tipo e a quantidade de informações necessárias para cada entrada. As implicações das entradas de ordenação em um perfil são explicadas em [perfis MAPI](mapi-profiles.md).
  
 **Para criar um perfil com código C ou C++**
  
1. Leia o arquivo de cabeçalho de cada serviço de mensagens. Entenda quais propriedades você precisará configurar e quais valores você usará.
    
2. Chame a função [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar um ponteiro de interface **IProfAdmin** . 
    
3. Chame [IProfAdmin:: CreateProfile](iprofadmin-createprofile.md) para criar seu perfil. Se você deseja criar um perfil com os serviços de mensagem listados na seção **[serviços padrão]** do MAPISVC. INF, defina o sinalizador MAPI_DEFAULT_SERVICE. Se você deseja permitir que o usuário insira informações de configuração, defina o sinalizador MAPI_DIALOG. Certifique-se de definir esse sinalizador se nem todas as informações necessárias estiverem disponíveis no MAPISVC. Arquivo INF. **CreateProfile** chama a função de ponto de entrada para cada serviço de mensagens a ser adicionado ao perfil com MSG_SERVICE_CREATE definido como o parâmetro _ulContext_ . 
    
4. Chame [IProfAdmin:: adminservices](iprofadmin-adminservices.md) para obter um objeto de administração de serviço de mensagens. 
    
5. Use o objeto de administração do serviço de mensagens para adicionar serviços de mensagens ao perfil. Para cada serviço de mensagens que você deseja adicionar:
    
1. Chame o método [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) para criar o novo serviço de mensagens. 
    
2. Call [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passando a estrutura **MAPIUID** do serviço que você acabou de criar e uma matriz de valor de propriedade com suas propriedades de configuração. 
    
6. Para recuperar o identificador de um serviço recém-adicionado, que é sua propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)), chame [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para acessar a tabela de serviço de mensagens e procure a linha que representa o serviço de mensagens. A última linha da tabela representará o serviço de mensagens mais recentemente adicionado. 
    
Para tornar um novo perfil temporário, chame o método [IProfAdmin::D eleteprofile](iprofadmin-deleteprofile.md) imediatamente após o logon. O **DeleteProfile** irá marcar o novo perfil como excluído, ao torná-lo utilizável durante a sessão. Como ele não será incluído na tabela de perfis da sessão, outros clientes não poderão usá-lo. 
  

