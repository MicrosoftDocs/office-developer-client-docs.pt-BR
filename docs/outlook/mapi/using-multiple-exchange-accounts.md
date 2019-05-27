---
title: Usar várias contas do Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: 'Última modificação: 25 de junho de 2012'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329649"
---
# <a name="using-multiple-exchange-accounts"></a>Usar várias contas do Exchange

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O Microsoft Outlook 2010 e o Microsoft Outlook 2013 incluem o suporte à integração com várias contas de email do Exchange. No Outlook 2010 ou no Outlook 2013, um usuário pode adicionar duas contas do Exchange ao mesmo perfil e ainda desfrutar dos recursos avançados do Exchange, como a GAL (lista de endereços global) publicada, a configuração de ausência temporária e o compartilhamento de pastas.
  
Aos que já conhecem as seções de perfil MAPI do Microsoft Office Outlook 2007 e anterior, sabem que as configurações do Exchange, como o nome de usuário e o nome do servidor de email, são armazenadas na seção de perfil global fixo do Exchange, ** pbGlobalProfileSectionGuid**. No Outlook 2010 e no Outlook 2013, cada conta do Exchange precisa da sua própria seção de perfil para armazenar as configurações, tornando o **pbGlobalProfileSectionGuid** obsoleto. 
  
As configurações do Outlook 2010 e do Outlook 2013 do Exchange ainda são armazenadas no perfil, mas um identificador exclusivo para a seção de perfil que contém suas configurações é alocado dinamicamente por perfil. O local das configurações do Exchange no perfil é armazenado na [propriedade canônica PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md), que pode ser encontrada na seção perfil de serviço de mensagens da conta do Exchange. Essa propriedade também pode ser encontrada na seção de perfil de cada provedor deste serviço de mensagem da conta. O identificador exclusivo não é armazenado no servidor e será diferente entre os perfis.
  
O Outlook 2010 e o Outlook 2013 usam o **PidTagExchangeProfileSectionId** como um identificador exclusivo para especificar uma conta do Exchange. Quando usado dessa maneira, esse identificador exclusivo é conhecido como o **emsmdbUID.** Para algumas operações MAPI e do Outlook, um **emsmdbUID** pode ser necessário para especificar qual conta do Exchange deve ser usada para a operação. 
  
Para suportar várias contas do Exchange, você deve usar algumas chamadas para novas funções no código. Substitua qualquer chamada que use um **entryID** e [IAddrBook::OpenEntry](iaddrbook-openentry.md) ou [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) em [IMailUser : IMAPIProp](imailuserimapiprop.md) e [IDistList : IMAPIContainer](idistlistimapicontainer.md) com uma das funções a seguir. 
  
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

Todos os clientes MAPI gravados antes da criação desta nova seção **emsmdbUID** ainda tem suporte. Esses clientes continuarão a recuperar a seção global anterior, **pbGlobalProfileSectionGuid**. As consultas para esta seção de perfil serão redirecionadas para uma conta designada do Exchange que manipula as consultas herdadas. A conta que manipula as chamadas herdadas pode ser determinada observando a tabela de serviço de mensagens e adicionando uma coluna para PR_EMSMDB_LEGACY. Somente um serviço de mensagem terá essa definição como verdadeira e seu **PidTagExchangeProfileSectionId** será chamado de **emsmdbUID** herdado.
  
> [!NOTE]
> As definições MAPI configuráveis, como o repositório e a conta padrão, não afetam a conta que manipula as chamadas herdadas. Não é possível configurar a conta que manipula as chamadas herdadas. 
  
A **emsmdbUID** da conta herdada será copiada para a seção de perfil global do Outlook. Se essa propriedade não existir, consultar a tabela de serviços de mensagem determinará qual conta é o manipulador herdado e definirá o valor na Seção de perfil global do Outlook. 
  
Para ser claro, a Seção de perfil global do Outlook é diferente da Seção de perfil global do Exchange, e no Outlook 2010 e no Outlook 2013 a Seção de perfil global do Exchange não é mais realmente global porque você pode ter várias contas do Exchange. A Seção de perfil global do Outlook contém propriedades sobre o Outlook, como o estado da pasta MRU ou o estado da conexão global.
  
## <a name="address-book-account-contexts"></a>Contextos da conta de catálogo de endereços

Para resolver os problemas corretamente com várias contas do Exchange, use as novas funções que usam um contexto de conta para que as chamadas ao catálogo de endereços pesquisem a conta correta do Exchange.
  
Algumas APIs de catálogo de endereços anteriores foram substituídas porque as APIs não eram totalmente compatíveis com várias contas do Exchange. Esse contexto de conta geralmente é uma **emsmdbUID**.
  
Além da **emsmdbUID**, as várias contas do Exchange também têm uma **emsabpUID**.
  
1. O valor **emsmdbUID** identifica o contexto da conta. 
    
2. O valor **emsabpUID** identifica um provedor de catálogo de endereços do Exchange. 
    
O valor **emsabpUID** geralmente é usado durante a resolução de um destinatário. Ao resolver um destinatário usando[IAddrBook::ResolveName](iaddrbook-resolvename.md), uma linha de destinatário do Exchange contém a propriedade **PR_AB_PROVIDERS** (0x3D010102), que contém o valor **emsabpUID**. Esse valor **emsabpUID** identifica o provedor de catálogo de endereços do Exchange para o destinatário específico. 
  
Se desejar determinar o valor **emsabpUID** de um determinado **emsmdbUID**, abra a seção de perfil do **emsmdbUID** e obtenha a propriedade **PR_EMSABP_ USER_UID** (0x0x3D1A0102). 
  
Se você estiver chamando [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), certifique-se de que os destinatários do Exchange na lista transmitida contêm a propriedade **PR_AB_PROVIDERS** que tem o **emsabpUID** que corresponde ao provedor do catálogo de endereços ao qual o destinatário pertence. Chamando [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) em uma linha que você obteve de [IAddrBook::ResolveName](iaddrbook-resolvename.md) não requer nenhuma ação adicional, mas algum código chamará [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) em linhas que contêm apenas a propriedade **PR_ENTRYID**. As linhas nesta e em situações similares devem conter **PR_ENTRYID** e **PR_AB_PROVIDERS** com a propriedade **PR_AB_PROVIDERS** definida como a **emsabpUID** correta.
  
Uma descrição simples do processo para resolver várias contas do Exchange é a seguinte:
  
- Devido ao identificador exclusivo do serviço, seu código procura na tabela do repositório de mensagens da propriedade **PR_SERVICE_UID** que corresponde àquela que você tem. A partir daí, você pode determinar a **PR_MDB_PROVIDER** correta. Esta linha contém o repositório apropriado.
    
- Devido a uma **emsmdbUID**, seu código procura na tabela de serviços de mensagem pela linha que expõe a **PidTagExchangeProfileSectionId** que corresponde ao **emsmdbUID**.
    
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

