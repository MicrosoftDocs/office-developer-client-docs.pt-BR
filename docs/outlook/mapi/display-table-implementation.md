---
title: Implementação da tabela de exibição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6990e32445083c3465693df2c1a3d40b980853c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435261"
---
# <a name="display-table-implementation"></a>Implementação da tabela de exibição

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela de exibição é usada para mostrar uma folha de propriedades, uma caixa de diálogo especial composta por uma ou mais páginas de propriedades com guias dedicadas à exibição e possivelmente edição de uma ou mais propriedades. Associado a cada tabela de exibição é uma implementação de interface [IAttach : IMAPIProp.](iattachimapiprop.md) A [implementação de IMAPIProp](imapipropiunknown.md) mantém os dados de propriedade apresentados na folha de propriedades. 
  
As linhas em uma tabela de exibição representam os controles na folha de propriedades. A maioria dos controles pode ser associada a propriedades mantidas com a **implementação IMAPIProp.** Quando um usuário altera o valor de um controle modificável, a propriedade correspondente é atualizada. 
  
As colunas em uma tabela de exibição representam propriedades do controle, como sua posição na folha de propriedades, seu tipo, estrutura associada e identificador. Para uma lista completa das colunas de tabela de exibição necessárias, consulte [Tabelas de Exibição.](display-tables.md)
  
MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly. Conforme o usuário trabalha com a folha de propriedades, alterando valores nos controles, MAPI chama [IMAPIProp::SetProps](imapiprop-setprops.md) para salvar um controle alterado se o sinalizador DT_SET_IMMEDIATE do controle estiver definido. Para controles sem o DT_SET_IMMEDIATE sinalizador definido, as alterações nas propriedades são salvas quando o usuário descarta a caixa de diálogo clicando no **botão OK** ou Aplicar **Agora.** Quando um desses botões ou o **botão Cancelar** é clicado, MAPI remove a folha de propriedades da exibição. 
  
MAPI obtém acesso à sua tabela de exibição chamando o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) na implementação **IMAPIProp** e solicitando a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) ou herdando-a em uma chamada que você fez para MAPI, como [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md).
  
A primeira técnica de acesso é usada quando os provedores de agendamento de endereço são solicitados a mostrar detalhes sobre usuários de mensagens ou listas de distribuição. Ocorre o seguinte processamento:
  
1. Um cliente chama o [método IAddrBook::D etails.](iaddrbook-details.md) 
    
2. MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry. 
    
3. MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box. 
    
4. MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished. 
    
## <a name="see-also"></a>Confira também



[Provedores de Serviços MAPI](mapi-service-providers.md)

