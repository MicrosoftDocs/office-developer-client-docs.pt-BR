---
title: One-Off tabelas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 8719536efa9bffb1226f8fb665b912eb872227f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439524"
---
# <a name="one-off-tables"></a>One-Off tabelas

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela única contém informações sobre os modelos que um provedor de agendas oferece suporte para a criação de novos destinatários. As tabelas individuais são implementadas por provedores de agendas de endereços, contêineres de agendas individuais e por MAPI e podem ser persistentes ou temporárias. 
  
> [!NOTE]
> Não confunda os modelos em tabelas one-off com identificadores de modelo; embora suas finalidades sejam semelhantes, suas construções de código não são nada parecidas. Os modelos são usados para criar destinatários de um tipo específico enquanto identificadores de modelo são usados para vincular os dados de um destinatário que pertencem a um provedor de host com código para dar suporte a outro destinatário que pertença a um provedor estrangeiro. 
  
Os clientes criam novos destinatários:
  
- Para adicionar à lista de destinatários de uma mensagem de saída.
    
- Para adicionar a um dos contêineres no livro de endereços.
    
Em ambos os cenários, um provedor de agendamento de endereços é solicitado a retornar uma tabela única. Os provedores de agenda podem implementar uma única tabela individual a ser usada em ambas as situações ou uma tabela única exclusiva para cada situação. 
  
Quando o destinatário for incluído com uma mensagem de saída, o MAPI chamará o método [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) do provedor de endereços para recuperar sua tabela única. A tabela única inclui modelos que permitem que um usuário insira informações que resultem na criação de um destinatário com um endereço válido. MapI registers for notifications on this table, keeping it open so that changes can be reflected to the user. MAPI releases the table only when its subsystem or address book status object's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called. 
  
Quando o destinatário será adicionado a um contêiner, o MAPI faz uma chamada diferente, invocando o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner para recuperar sua propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). O conjunto de modelos incluídos nesta tabela única representa os tipos de destinatários que podem ser adicionados ao contêiner. Por exemplo, os servidores de email frequentemente expõem um contêiner para cada gateway instalado para que cada contêiner mantenha apenas endereços específicos para o gateway correspondente.
  
MAPI provides a one-off table that includes its own templates as well as templates from each of the address book providers in the session. MAPI provides a generic template that can be used to create a new recipient for any address type, assuming that the user knows its format. Os provedores de agendamento de endereço usam esta tabela única chamando [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md). Cada um dos modelos incluídos na tabela única MAPI resulta na criação de destinatários com endereços de destinatário válidos.
  
Os provedores de agendas geralmente fornecem um modelo para cada tipo de endereço ao qual suportam. No entanto, o suporte para modelos não é necessário. Os provedores de agendas que não permitem a criação de novos endereços podem retornar MAPI_E_NO_SUPPORT chamadas MAPI para solicitar uma tabela única. Os provedores de agendamento de endereço que permitem a criação de novos endereços, mas não fornecem modelos, podem chamar **IMAPISupport::GetOneOffTable** para usar os modelos listados na tabela única MAPI. 
  
As propriedades a seguir compom o conjunto de colunas necessário em tabelas únicas:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md))
    
 **PR_ADDRTYPE** indica o tipo de endereço que pode ser associado ao novo destinatário criado com o modelo. 
  
 **PR_DISPLAY_NAME** e **PR_DISPLAY_TYPE** dados associados ao novo destinatário. **PR_DISPLAY_NAME** contém uma cadeia de caracteres que identifica o novo **destinatário e PR_DISPLAY_TYPE** contém uma constante que identifica o tipo de ícone a ser exibido com a linha. Modelos para usuários de mensagens têm suas **colunas PR_DISPLAY_TYPE** definidas como DT_MAILUSER; os modelos de listas de distribuição **têm** PR_DISPLAY_TYPE coluna definida como DT_DISTLIST. 
  
 **PR_ENTRYID** é o identificador de entrada do modelo a ser usado para criar um novo destinatário. Esse identificador de entrada pode ser passado para futuras [chamadas IAddrBook::NewEntry](iaddrbook-newentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md)e [IABContainer::CreateEntry.](iabcontainer-createentry.md) Os contêineres configuram PR_ENTRYID coluna **de** sua linha para o modelo de usuário de mensagens padrão como **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) e **PR_ENTRYID** coluna de sua linha para o modelo de lista de distribuição padrão como **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). 
  
 **PR_DEPTH** é usado para dar suporte à exibição hierárquica das entradas em uma tabela única, indicando o nível de recuo do modelo. Embora as tabelas um-off possam ser exibidas como uma lista simples ou uma exibição hierárquica, a última é preferível e os provedores de agenda devem dar suporte a ela definindo a coluna **PR_DEPTH** para cada linha adequadamente. **PR_DEPTH** é baseado em zero; linhas com um valor 0 em sua **PR_DEPTH** coluna não são recuadas. Quanto maior o valor **de PR_DEPTH**, mais a linha será recuada. Por exemplo, linhas com **PR_DEPTH** definidas como 1 são recuadas  uma guia enquanto as linhas com PR_DEPTH definidas como 3 são recuadas três guias. 
  
 **PR_SELECTABLE** é usado para indicar se uma linha na tabela representa um modelo que pode ser selecionado e usado para criar um novo destinatário. Embora a maioria das linhas em uma tabela única represente modelos, os provedores podem incluir linhas que não são de modelo. Por exemplo, um provedor pode querer organizar a tabela única por tipo de modelo, incluindo uma linha de categoria que aparece na exibição, mas não é usada para a criação de destinatários. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

