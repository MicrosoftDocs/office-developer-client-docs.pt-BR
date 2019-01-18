---
title: Usar várias contas do Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: 'Última modificação: 25 de julho de 2012'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723058"
---
# <a name="using-multiple-exchange-accounts"></a>Usar várias contas do Exchange

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook 2010 e o Microsoft Outlook 2013 suportam integração com várias contas de email do exchange. No Outlook 2010 ou Outlook 2013, um usuário pode adicionar duas contas do exchange para o mesmo perfil e ainda aproveitar os recursos avançados do Exchange como a lista publicada de endereços global (GAL), a configuração do Exchange de ausência temporária e compartilhamento de pastas.
  
Esses familiarizado com as seções de perfil MAPI do Microsoft Office Outlook 2007 e versões anteriores sabem que as configurações do Exchange, como o nome de usuário de email e o nome do servidor, são armazenadas na seção perfil Global do Exchange fixa, **pbGlobalProfileSectionGuid**. No Outlook 2010 e o Outlook 2013, cada conta Exchange precisa sua própria seção de perfil para armazenar as configurações, tornando o **pbGlobalProfileSectionGuid** obsoleto. 
  
Configurações do Outlook 2010 e o Outlook 2013 Exchange ainda são armazenadas no perfil, mas um identificador exclusivo para a seção de perfil que contém suas configurações, que é alocado dinamicamente por perfil. A localização das configurações do Exchange no perfil é armazenada na [Propriedade canônico de PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md), que podem ser encontradas na seção de perfil de serviço de mensagem da conta do Exchange. Essa propriedade também pode ser encontrada na seção de perfil de cada provedor neste serviço de mensagem da conta. O identificador exclusivo não está armazenado no servidor e será diferente nos perfis.
  
Outlook 2010 e o Outlook 2013 usam o **PidTagExchangeProfileSectionId** como um identificador exclusivo para especificar uma conta do Exchange. Quando usado dessa maneira, esse identificador exclusivo é conhecido como o **emsmdbUID**. Para algumas operações MAPI e o Outlook, um **emsmdbUID** pode ser necessária para especificar qual conta Exchange deve ser usada para a operação. 
  
Para oferecer suporte a várias contas do Exchange, você deve usar algumas chamadas para novas funções em seu código. Substitua qualquer chamada que usa uma **entryID** e [IAddrBook::OpenEntry](iaddrbook-openentry.md) ou [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) em [IMailUser: IMAPIProp](imailuserimapiprop.md) e [IDistList: IMAPIContainer](idistlistimapicontainer.md) com uma das funções a seguir. 
  
- [HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
    
- [HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
    
- [HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
    
- [HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
    
- [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
    
- [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
    
- [HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
    
- [HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
    
- [HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a>Suporte de legado

Todos os clientes MAPI escritos antes da criação da nova seção **emsmdbUID** ainda são suportados. Esses clientes continuarão recuperar a seção global anterior, **pbGlobalProfileSectionGuid**. Consultas para esta seção de perfil serão redirecionadas para uma conta do Exchange designada que processa consultas herdadas. A conta que processa as chamadas herdadas pode ser determinada olhando a tabela de serviços de mensagem e adicionando uma coluna para PR_EMSMDB_LEGACY. Somente um serviço de mensagem terá essa definição como true e seu **PidTagExchangeProfileSectionId** é chamado de legado **emsmdbUID**.
  
> [!NOTE]
> Configurações de MAPI configuráveis, como o repositório padrão e a conta padrão não têm efeito no qual a conta processa as chamadas de legado. A conta que processa as chamadas herdadas não pode ser configurada. 
  
O **emsmdbUID** da conta herdada é copiado para a seção perfil Global do Outlook. Se essa propriedade não existir, consultando a tabela de serviços de mensagens determinar qual conta está o manipulador de legado e defina o valor na seção Global do perfil do Outlook. 
  
Seja claro, a seção de perfil do Outlook Global difere a seção de perfil Global do Exchange e no Outlook 2010 e o Outlook 2013 a seção de perfil Global do Exchange não é mais realmente global porque é possível ter várias contas do Exchange. A seção de perfil do Outlook Global contém propriedades sobre o Outlook, como o estado da pasta MRU ou o estado da conexão a global.
  
## <a name="address-book-account-contexts"></a>Contextos de contas do catálogo de endereços

Para resolver endereços corretamente com várias contas do Exchange, use as novas funções que obtenha um contexto de conta, para que a conta do Exchange correta de pesquisa de chamadas para o catálogo de endereços.
  
Alguns catálogo de endereços anterior que APIs foram preteridas porque as APIs não foram totalmente vários Exchange capaz. Nesse contexto da conta geralmente é um **emsmdbUID**.
  
Além do **emsmdbUID**, várias contas do Exchange também têm um **emsabpUID**.
  
1. O valor de **emsmdbUID** identifica o contexto de conta. 
    
2. O valor de **emsabpUID** identifica um fornecedor de catálogo de endereços do Exchange. 
    
O valor de **emsabpUID** geralmente é usado ao resolver um destinatário. Ao resolver um destinatário usando [IAddrBook::ResolveName](iaddrbook-resolvename.md), uma linha de destinatário do Exchange contém a propriedade **PR_AB_PROVIDERS** (0x3D010102), que contém o valor de **emsabpUID** . Esse valor **emsabpUID** identifica o provedor de catálogo de endereços do Exchange para o destinatário específico. 
  
Se você deseja determinar o valor de **emsabpUID** para um determinado **emsmdbUID**, abra a seção de perfil para o **emsmdbUID** e obter a propriedade **PR_EMSABP_USER_UID** (0x0x3D1A0102). 
  
Se você estiver chamando [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), certifique-se de que os destinatários do Exchange na lista que você passar em contenham a propriedade **PR_AB_PROVIDERS** que tem o **emsabpUID** que corresponde ao provedor de catálogo de endereços que o destinatário pertence. Chamar [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) em uma linha que você obteve de [IAddrBook::ResolveName](iaddrbook-resolvename.md) requer nenhuma ação adicional, mas alguns códigos chamará [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) em linhas que contêm apenas **PR_ENTRYID** propriedade. Linhas neste e situações semelhantes devem conter **PR_ENTRYID** e o **PR_AB_PROVIDERS** com a propriedade **PR_AB_PROVIDERS** definida como o correto **emsabpUID**.
  
Uma descrição simples do que o processo de resolução de várias contas do Exchange é o seguinte:
  
- Dado o identificador exclusivo do serviço, seu código procura no índice de armazenamento de mensagens da propriedade **PR_SERVICE_UID** que corresponde ao que você precisa. A partir daí, você pode determinar o correto **PR_MDB_PROVIDER**. Esta linha contém o store apropriado.
    
- Dado um **emsmdbUID**, seu código procura na tabela de serviços de mensagem para a linha que expõe a **PidTagExchangeProfileSectionId** que corresponde a **emsmdbUID**.
    
## <a name="see-also"></a>Confira também



[HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
  
[HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
  
[HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
  
[HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
  
[HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
  
[HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
  
[HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
  
[HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
  
[HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
  
[HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
  
[Propriedade canônica PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md)


[Como abrir a seção perfil Global](https://support.microsoft.com/kb/188482)

