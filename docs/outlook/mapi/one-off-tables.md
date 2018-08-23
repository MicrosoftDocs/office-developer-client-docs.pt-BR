---
title: Tabelas únicas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: 'Modificado pela última vez: 08 de novembro de 2011'
ms.openlocfilehash: fc8d8d53dcbc091df98ba9e23533e4138660c8e2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574563"
---
# <a name="one-off-tables"></a>Tabelas únicas

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela único contém informações sobre os modelos de um provedor de catálogo de endereços oferece suporte para a criação de novos destinatários. Tabelas únicas são implementadas por provedores de catálogo de endereços, recipientes do catálogo de endereços individuais e MAPI e podem ser persistente ou temporária. 
  
> [!NOTE]
> Não confunda os modelos nas tabelas únicos com identificadores de modelo; enquanto seus objetivos são semelhantes, suas construções de código são semelhantes nothing. Modelos são usados para criar os destinatários de um determinado tipo enquanto os identificadores de modelo são usados para associar os dados de um destinatário que pertencem a um provedor de host com o código para dar suporte a outro destinatário que pertencem a um provedor de estrangeiro. 
  
Clientes criar novos destinatários:
  
- Para adicionar à lista de destinatários de uma mensagem de saída.
    
- Para adicionar um dos contêineres no catálogo de endereços.
    
Em ambos os cenários, um provedor de catálogo de endereços é solicitado para retornar uma tabela único. Provedores de catálogo de endereços podem implementar em uma única tabela único para ser usado em situações tanto ou uma tabela único exclusiva para cada situação. 
  
Quando o destinatário será incluído em uma mensagem de saída, MAPI chama o método de [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) do provedor de catálogo de endereços para recuperar sua tabela único. A tabela único inclui modelos que permitem ao usuário inserir informações resultando na criação de um destinatário com um endereço válido. Registradores MAPI para notificações sobre esta tabela, mantendo-abrir para que as alterações podem ser refletidas ao usuário. MAPI libera a tabela somente quando o método de [IMAPIStatus::ValidateState](imapistatus-validatestate.md) seu subsistema ou endereço livro status do objeto é chamado. 
  
Quando o destinatário será adicionado a um contêiner, o MAPI faz uma chamada diferente, invocar o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner para recuperar sua propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). O conjunto de modelos incluídos nesta tabela único representa os tipos de destinatários que podem ser adicionados ao contêiner. Por exemplo, servidores de email com frequência exponham um contêiner para cada gateway que é instalado para que cada contêiner somente contém os endereços específicos para o gateway correspondente.
  
MAPI fornece uma tabela único que inclui seus próprios modelos, bem como os modelos de cada um dos provedores de catálogo de endereços na sessão. MAPI fornece um modelo genérico que pode ser usado para criar um novo destinatário para qualquer tipo de endereço, supondo que o usuário saiba o seu formato. Provedores de catálogo de endereços usam esta tabela único chamando [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md). Cada um dos modelos incluídos nos resultados da tabela únicos MAPI na criação de destinatários com os endereços de destinatário válidos.
  
Normalmente, provedores de catálogo de endereços fornecem um modelo para cada tipo de endereço que eles suportam. No entanto, o suporte para modelos não é necessária. Provedores de catálogo de endereços que não permitem a criação de novos endereços podem retornar MAPI_E_NO_SUPPORT quando chamadas de MAPI para solicitar uma tabela único. Provedores de catálogo de endereços que permite a criação de endereço novo, mas não fornecer quaisquer modelos podem chamar **IMAPISupport::GetOneOffTable** para usar os modelos listados na tabela único MAPI. 
  
As seguintes propriedades compõem a coluna necessária definida nas tabelas únicas:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md))
    
 **PR_ADDRTYPE** indica o tipo de endereço que pode ser associado com o novo destinatário criado com o modelo. 
  
 **PR_DISPLAY_NAME** e **PR_DISPLAY_TYPE** associar dados com o novo destinatário. **PR_DISPLAY_NAME** contém uma cadeia de caracteres que identifica o novo destinatário e **PR_DISPLAY_TYPE** contém uma constante que identifica o tipo de ícone a ser exibido com a linha. Modelos para mensagens de usuários têm sua coluna **PR_DISPLAY_TYPE** definida como DT_MAILUSER; modelos para listas de distribuição têm sua coluna **PR_DISPLAY_TYPE** definida como DT_DISTLIST. 
  
 **PR_ENTRYID** é o identificador de entrada do modelo a ser usado para criar um novo destinatário. Esse identificador de entrada pode ser passado para chamadas [IAddrBook::NewEntry](iaddrbook-newentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md)e [IABContainer::CreateEntry](iabcontainer-createentry.md) futuras. Configure o contêineres column **PR_ENTRYID** da sua linha para o padrão de modelo de usuário para **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) e a coluna **PR_ENTRYID** da sua linha na lista de distribuição padrão de mensagens modelo deve ser **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). 
  
 **PR_DEPTH** é usado para apoiar a exibição hierárquica das entradas em uma tabela único indicando o nível de recuo para o modelo. Embora tabelas únicas podem ser exibidas como uma lista simples ou uma exibição hierárquica, o último é preferível e provedores de catálogo de endereços devem oferecer suporte a ele, definindo a coluna **PR_DEPTH** para cada linha apropriadamente. **PR_DEPTH** é baseado em zero; linhas com um valor 0 na coluna seus **PR_DEPTH** não são recuadas. Quanto maior o valor de **PR_DEPTH**, mais a linha é recuada. Por exemplo, linhas com **PR_DEPTH** definida como 1 são recuado uma guia enquanto linhas com **PR_DEPTH** definido como 3 estão recuados três guias. 
  
 **PR_SELECTABLE** é usado para indicar se uma linha da tabela representa um modelo que pode ser selecionado e usado para criar um novo destinatário. Embora a maioria das linhas em uma tabela único representam modelos, provedores podem incluir linhas não-template. Por exemplo, um provedor talvez queira organizar a tabela único por tipo de modelo, incluindo uma linha de categoria que aparece na exibição, mas não é usada para a criação de destinatário. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

