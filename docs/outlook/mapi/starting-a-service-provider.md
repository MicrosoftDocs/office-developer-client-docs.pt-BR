---
title: Iniciar um provedor de serviços
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: 'Última modificação: 07 de dezembro de 2015'
ms.openlocfilehash: d14a9961002d63733423af474e147ec5001051fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586330"
---
# <a name="starting-a-service-provider"></a>Iniciar um provedor de serviços

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Em algum momento depois que um cliente inicia uma sessão com MAPI, seu provedor de serviços será iniciado. Provedores de transporte são iniciados quando um cliente faz uma solicitação para seus serviços. Provedores de armazenamento de mensagens e catálogo de endereço são iniciados durante o processo de logon do cliente.
  
Um cliente chama [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) para carregar a cada um dos provedores de catálogo de endereços incluídos no perfil e [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) para carregar um provedor de armazenamento de mensagem específica. Os provedores que fazem parte de um serviço de mensagem foram iniciados antes de qualquer um dos outros provedores no serviço de catálogo de endereços. 
  
MAPI inicia cada provedor de serviços no perfil ativo, fazendo o seguinte:
  
- Localizando o nome do seu DLL no perfil. É necessário para registrar o nome do seu provedor de DLL no arquivo de configuração para garantir que ele aparece no perfil Mapisvc. Quando seu provedor de serviço é adicionado a um perfil, individualmente ou como parte de um serviço de mensagem, todas as seções **[Provedor de serviço]** do Mapisvc que se aplicam ao seu provedor são copiadas para o perfil. Para obter mais informações sobre a estrutura de Mapisvc, consulte o [Formato de arquivo do Mapisvc](file-format-of-mapisvc-inf.md).
    
- Chamar a função de API do Windows **LoadLibrary** , carregar a DLL. Porque as chamadas de MAPI **LoadLibrary** alguma toda vez que ele usa um provedor de serviço DLL (independente se já tiver sido carregada) ou somente na primeira vez, seu provedor de serviços não deve fazer suposições sobre o número de vezes que será carregado. Para cada chamada a **LoadLibrary**, MAPI faz uma chamada para a função de API do Windows **FreeLibrary** quando um provedor de serviços que dll não é mais necessária. 
    
- Chamar a função de ponto de entrada para o provedor. MAPI chama a função de ponto de entrada do seu provedor para iniciar o processo de logon. Funções de ponto de entrada Certifique-se de que você está usando uma versão da interface do provedor de serviço (SPI) que seja compatível com a versão que está sendo usada pelo MAPI. Essas funções retornam também ponteiros para objetos do provedor recém-criado. Para obter mais informações sobre como criar uma entrada ponto função para seu provedor, consulte [Implementando uma função de ponto de entrada do serviço provedor](implementing-a-service-provider-entry-point-function.md).
    
## <a name="see-also"></a>Confira também



[Provedores de serviços MAPI](mapi-service-providers.md)

