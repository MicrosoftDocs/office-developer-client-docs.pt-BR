---
title: Tabelas únicas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: 'Última modificação: 08 de novembro de 2011'
ms.openlocfilehash: 8719536efa9bffb1226f8fb665b912eb872227f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439524"
---
# <a name="one-off-tables"></a>Tabelas únicas

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela única contém informações sobre os modelos que um provedor de catálogo de endereços oferece suporte para a criação de novos destinatários. As tabelas únicas são implementadas por provedores de catálogo de endereços, contêineres de catálogos de endereços individuais e MAPI e podem ser persistentes ou temporárias. 
  
> [!NOTE]
> Não confunda os modelos em tabelas únicas com identificadores de modelo; Embora seus propósitos sejam semelhantes, suas construções de código não são semelhantes. Os modelos são usados para criar destinatários de um tipo específico enquanto os identificadores de modelo são usados para vincular os dados de um destinatário que pertencem a um provedor de host com código para dar suporte a outro destinatário que pertença a um provedor estrangeiro. 
  
Os clientes criam novos destinatários:
  
- Para adicionar à lista de destinatários de uma mensagem de saída.
    
- Para adicionar a um dos contêineres no catálogo de endereços.
    
Em ambos os cenários, um provedor de catálogo de endereços é solicitado a retornar uma tabela única. Os provedores de catálogos de endereços podem implementar uma única tabela única para ser usada em ambas as situações ou uma tabela única exclusiva para cada situação. 
  
Quando o destinatário for incluído em uma mensagem de saída, o MAPI chamará o método [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) do provedor de catálogo de endereços para recuperar sua tabela única. A tabela única inclui modelos que permitem que um usuário insira informações que resultam na criação de um destinatário com um endereço válido. O MAPI registra para notificações nesta tabela, mantendo-a aberta para que as alterações possam ser refletidas para o usuário. MAPI libera a tabela somente quando o método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) do objeto de status do seu subsistema ou catálogo de endereços é chamado. 
  
Quando o destinatário for adicionado a um contêiner, o MAPI fará uma chamada diferente, invocando o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) do contêiner para recuperar sua propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). O conjunto de modelos incluídos nessa tabela única representa os tipos de destinatários que podem ser adicionados ao contêiner. Por exemplo, os servidores de email geralmente expõem um contêiner para cada gateway instalado de modo que cada contêiner só tenha endereços específicos para o gateway correspondente.
  
O MAPI fornece uma tabela única que inclui seus próprios modelos, bem como modelos de cada provedor de catálogo de endereços na sessão. O MAPI fornece um modelo genérico que pode ser usado para criar um novo destinatário para qualquer tipo de endereço, supondo que o usuário sabe seu formato. Os provedores de catálogo de endereços usam essa tabela única chamando [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md). Cada um dos modelos incluídos na tabela unificada de MAPI resulta na criação de destinatários com endereços de destinatários válidos.
  
Geralmente, os provedores de catálogo de endereços fornecem um modelo para cada tipo de endereço que eles suportam. No enTanto, o suporte para modelos não é necessário. Os provedores de catálogo de endereços que não permitem a criação de novos endereços podem retornar MAPI_E_NO_SUPPORT quando as chamadas MAPI solicitam uma tabela única. Os provedores de catálogo de endereços que permitem a criação de novos endereços, mas não fornecem nenhum modelo podem chamar **IMAPISupport:: GetOneOffTable** para usar os modelos listados na tabela de one-off MAPI. 
  
As propriedades a seguir compõem o conjunto de colunas necessárias em tabelas únicas:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md))
    
 **PR_ADDRTYPE** indica o tipo de endereço que pode ser associado ao novo destinatário criado com o modelo. 
  
 **PR_DISPLAY_NAME** e **PR_DISPLAY_TYPE** associam dados ao novo destinatário. **PR_DISPLAY_NAME** contém uma cadeia de caracteres que identifica o novo destinatário e **PR_DISPLAY_TYPE** contém uma constante que identifica o tipo de ícone a ser exibido com a linha. Modelos para usuários de mensagens têm sua coluna **PR_DISPLAY_TYPE** definida como DT_MAILUSER; modelos para listas de distribuição têm suas colunas **PR_DISPLAY_TYPE** definidas como DT_DISTLIST. 
  
 **PR_ENTRYID** é o identificador de entrada do modelo a ser usado para criar um novo destinatário. Este identificador de entrada pode ser passado para o futuro [IAddrBook:: NewEntry](iaddrbook-newentry.md), [IAddrBook:: OpenEntry](iaddrbook-openentry.md)e [IABContainer:: createentry](iabcontainer-createentry.md) calls. Os contêineres definem a coluna **PR_ENTRYID** de suas linhas para o modelo de usuário de mensagens padrão como **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) e a coluna **PR_ENTRYID** de suas linhas para a lista de distribuição padrão modelo para **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). 
  
 **PR_DEPTH** é usado para oferecer suporte à exibição hierárquica das entradas em uma tabela única, indicando o nível de recuo para o modelo. Embora tabelas individuais possam ser exibidas como uma lista simples ou uma exibição hierárquica, a última é que os provedores de catálogo de endereços e preferíveis devem oferecer suporte à configuração da coluna **PR_DEPTH** para cada linha apropriadamente. **PR_DEPTH** é baseado em zero; as linhas com um valor 0 na coluna **PR_DEPTH** não são recuadas. Quanto maior o valor de **PR_DEPTH**, mais a linha é recuada. Por exemplo, as linhas com **PR_DEPTH** definidas como 1 são recuadas uma Tabulação enquanto as linhas com **PR_DEPTH** definidas como 3 são recuadas três guias. 
  
 **PR_SELECTABLE** é usado para indicar se uma linha na tabela representa um modelo que pode ser selecionado e usado para criar um novo destinatário. Embora a maioria das linhas em uma tabela única represente modelos, os provedores podem incluir linhas que não são do modelo. Por exemplo, um provedor pode querer organizar a tabela única por tipo de modelo, incluindo uma linha de categoria que aparece na exibição, mas não é usada para a criação de destinatários. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

