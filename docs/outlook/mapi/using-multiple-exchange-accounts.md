---
title: Usando várias contas do Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329649"
---
# <a name="using-multiple-exchange-accounts"></a>Usando várias contas do Exchange

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook 2010 e Microsoft Outlook 2013 oferecem suporte à integração com várias contas de email do Exchange. No Outlook 2010 ou no Outlook 2013, um usuário pode adicionar duas contas do Exchange ao mesmo perfil e ainda desfrutar de recursos avançados do Exchange, como a GAL (lista de endereços global) publicada, a configuração de ausência temporária do Exchange e o compartilhamento de pasta.
  
Aqueles familiarizados com as seções de perfil MAPI para o Microsoft Office Outlook 2007 e anteriores sabem que as configurações do Exchange, como o nome de usuário e o nome do servidor de email, são armazenadas na seção perfil global do Exchange fixo, **pbGlobalProfileSectionGuid**. No Outlook 2010 e no Outlook 2013, cada conta do Exchange precisa de sua própria seção de perfil para armazenar as configurações, tornando o **pbGlobalProfileSectionGuid** obsoleto. 
  
As configurações do Outlook 2010 e do Outlook 2013 Exchange ainda estão armazenadas no perfil, mas um identificador exclusivo para a seção de perfil que contém suas configurações é alocado dinamicamente por perfil. O local das configurações do Exchange no perfil é armazenado na [Propriedade canônica PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md), que pode ser encontrada na seção perfil de serviço de mensagens da conta do Exchange. Essa propriedade também pode ser encontrada na seção perfil de cada provedor neste serviço de mensagens da conta. O identificador exclusivo não é armazenado no servidor e será diferente nos perfis.
  
O Outlook 2010 e o Outlook 2013 usam o **PidTagExchangeProfileSectionId** como um identificador exclusivo para especificar uma conta do Exchange. Quando usado dessa maneira, esse identificador exclusivo é conhecido como **emsmdbUID**. Para algumas operações MAPI e do Outlook, um **emsmdbUID** pode ser necessário para especificar qual conta do Exchange deve ser usada para a operação. 
  
Para dar suporte a várias contas do Exchange, você deve usar algumas chamadas para novas funções no seu código. Substitua qualquer chamada que use uma **EntryID** e [IAddrBook:: OpenEntry](iaddrbook-openentry.md) ou [IAddrBook:: CompareEntryIDs](iaddrbook-compareentryids.md) no [IMailUser: IMAPIProp](imailuserimapiprop.md) e [IDistList: IMAPIContainer](idistlistimapicontainer.md) com uma das seguintes funções. 
  
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
    
## <a name="legacy-support"></a>Suporte herdado

Todos os clientes MAPI gravados antes da criação dessa nova seção **emsmdbUID** ainda são suportados. Esses clientes continuarão a recuperar a seção global anterior, **pbGlobalProfileSectionGuid**. As consultas para esta seção de perfil serão redirecionadas para uma conta do Exchange designada que lide com as consultas herdadas. A conta que manipula as chamadas herdadas pode ser determinada examinando a tabela de serviço de mensagens e adicionando uma coluna para PR_EMSMDB_LEGACY. Apenas um serviço de mensagens terá essa definição como true e seu **PidTagExchangeProfileSectionId** será chamado de **emsmdbUID**herdado.
  
> [!NOTE]
> As configurações de MAPI configuráveis, como o repositório padrão e a conta padrão, não têm efeito sobre qual conta lida com chamadas herdadas. A conta que manipula as chamadas herdadas não pode ser configurada. 
  
A **emsmdbUID** da conta herdada é copiada para a seção de perfil global do Outlook. Se essa propriedade não existir, a consulta à tabela de serviços de mensagem determinará qual é a conta do manipulador herdado e definirá o valor na seção de perfil global do Outlook. 
  
Para ser claro, a seção de perfil global do Outlook difere da seção de perfil global do Exchange e no Outlook 2010 e Outlook 2013 a seção de perfil global do Exchange não é mais realmente global porque você pode ter várias contas do Exchange. A seção de perfil global do Outlook contém propriedades sobre o Outlook, como o estado da pasta MRU ou o estado da conexão global.
  
## <a name="address-book-account-contexts"></a>Contextos de conta de catálogo de endereços

Para resolver endereços corretamente com várias contas do Exchange, use as novas funções que usam um contexto de conta para que as chamadas ao catálogo de endereços pesquisem a conta correta do Exchange.
  
Algumas APIs anteriores do catálogo de endereços foram preteridas porque as APIs não tinham totalmente vários recursos do Exchange. Este contexto de conta geralmente é um **emsmdbUID**.
  
Além do **emsmdbUID**, várias contas do Exchange também têm um **emsabpUID**.
  
1. O valor **emsmdbUID** identifica o contexto da conta. 
    
2. O valor **emsabpUID** identifica um provedor do catálogo de endereços do Exchange. 
    
O valor **emsabpUID** normalmente é usado durante a resolução de um destinatário. Ao resolver um destinatário usando [IAddrBook:: ResolveName](iaddrbook-resolvename.md), uma linha de destinatário do Exchange contém a propriedade **PR_AB_PROVIDERS** (0x3D010102), que contém o valor de **emsabpUID** . Esse valor **emsabpUID** identifica o provedor de catálogo de endereços do Exchange para o destinatário específico. 
  
Se você quiser determinar o valor de **emsabpUID** para um determinado **emsmdbUID**, abra a seção de perfil para o **EmsmdbUID** e obtenha a propriedade **PR_EMSABP_USER_UID** (0x0x3D1A0102). 
  
Se você estiver chamando [IAddrBook::P reparerecips](iaddrbook-preparerecips.md), certifique-se de que os destinatários do Exchange na lista que você aprovou contenham a propriedade **PR_AB_PROVIDERS** que tem o **emsabpUID** que corresponde ao provedor de catálogo de endereços que o destinatário pertence. Chamar [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) em uma linha Obtida de [IAddrBook:: resolvedor](iaddrbook-resolvename.md) não requer nenhuma ação adicional, mas um código chamará [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) em linhas que contenham apenas o **PR_ENTRYID** Propriedades. As linhas nessas e situações semelhantes devem conter **PR_ENTRYID** e **PR_AB_PROVIDERS** com a propriedade **PR_AB_PROVIDERS** definida como o **emsabpUID**correto.
  
Uma descrição simples do processo para resolver várias contas do Exchange é a seguinte:
  
- Dado o identificador exclusivo do serviço, seu código procura na tabela do repositório de mensagens da propriedade **PR_SERVICE_UID** que corresponde à que você tem. A partir daí, é possível determinar o **PR_MDB_PROVIDER**correto. Esta linha contém o repositório apropriado.
    
- Dado um **emsmdbUID**, seu código procura na tabela de serviços de mensagem da linha que expõe o **PidTagExchangeProfileSectionId** que corresponde ao **emsmdbUID**.
    
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


[Como abrir a seção de perfil global](https://support.microsoft.com/kb/188482)

