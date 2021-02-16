---
title: Iniciando um provedor de serviços
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: f67976681ef0283c86e1c09c49e531572668ff50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439552"
---
# <a name="starting-a-service-provider"></a>Iniciando um provedor de serviços

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Em algum momento após um cliente iniciar uma sessão com MAPI, seu provedor de serviços será iniciado. Os provedores de transporte são iniciados quando um cliente faz uma solicitação para seus serviços. Os provedores do address book e do armazenamento de mensagens são iniciados durante o processo de logon do cliente.
  
Um cliente chama [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) para carregar cada um dos provedores de agendas incluídos no perfil e [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) para carregar um provedor de repositório de mensagens específico. Os provedores de agendas que fazem parte de um serviço de mensagens são iniciados antes de qualquer um dos outros provedores no serviço. 
  
O MAPI inicia cada provedor de serviços no perfil ativo fazendo o seguinte:
  
- Localizar o nome de sua DLL no perfil. Você precisa registrar o nome de seu provedor DLL no arquivo de configuração Mapisvc.inf para garantir que ele apareça no perfil. Quando seu provedor de serviços é adicionado a um perfil, individualmente ou como parte de um serviço de mensagens, todas as seções [Provedor de **Serviços]** de Mapisvc.inf que se aplicam ao seu provedor são copiadas para o perfil. Para obter mais informações sobre a estrutura de Mapisvc.inf, consulte o formato de [arquivo de MapiSvc.inf](file-format-of-mapisvc-inf.md).
    
- Chamar a função **LoadLibrary** da API do Windows para carregar a DLL. Como o MAPI chama **LoadLibrary** sempre que usa uma DLL do provedor de serviços (independentemente de já ter sido carregada) ou apenas na primeira vez, seu provedor de serviços não deve fazer suposições sobre o número de vezes que ele será carregado. Para cada chamada para **LoadLibrary**, o MAPI faz uma chamada para a função da API do Windows **FreeLibrary** quando uma DLL do provedor de serviços não é mais necessária. 
    
- Chamar a função de ponto de entrada para o provedor. O MAPI chama a função de ponto de entrada do provedor para iniciar o processo de logon. As funções de ponto de entrada garantem que você está usando uma versão da interface do provedor de serviços (SPI) compatível com a versão usada pelo MAPI. Essas funções também retornam ponteiros para objetos de provedor recém-criados. Para obter mais informações sobre como criar uma função de ponto de entrada para seu provedor, consulte Implementando uma função de ponto de entrada do provedor [de serviços.](implementing-a-service-provider-entry-point-function.md)
    
## <a name="see-also"></a>Confira também



[Provedores de Serviços MAPI](mapi-service-providers.md)

