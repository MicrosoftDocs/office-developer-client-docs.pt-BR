---
title: Implementação da tabela de exibição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 07ad94c423c3be425dc905dc578f55ad2c467a95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766413"
---
# <a name="display-table-implementation"></a>Implementação da tabela de exibição

  
  
**Aplica-se a**: Outlook 
  
Uma tabela de exibição é usada para mostrar uma folha de propriedades, uma caixa de diálogo especial é composta de um ou mais páginas com guias Propriedade dedicada ao exibindo e editando possivelmente uma ou mais propriedades. Associados com cada exibição tabela é um [IAttach: IMAPIProp](iattachimapiprop.md) implementação de interface. A implementação de [IMAPIProp](imapipropiunknown.md) mantém os dados de propriedade apresentada na folha de propriedades. 
  
As linhas em uma tabela de exibição representam os controles na folha de propriedades. A maioria dos controles pode ser associado com propriedades mantidas com a implementação de **IMAPIProp** . Quando um usuário altera o valor de um controle modificável, a propriedade correspondente é atualizada. 
  
As colunas em uma tabela de exibição representam as propriedades do controle, como sua posição na folha de propriedades, seu tipo, estrutura associada e identificador. Para obter uma lista completa das colunas da tabela de exibição necessários, consulte [Exibir tabelas](display-tables.md).
  
MAPI exibe uma folha de propriedades para o usuário de um aplicativo cliente lendo valores de propriedade da implementação **IMAPIProp** associado à tabela de exibição ou da tabela de exibição diretamente. Conforme o usuário trabalha com a folha de propriedades, alterando os valores nos controles, MAPI chama [IMAPIProp::SetProps](imapiprop-setprops.md) para salvar um controle alterado se o sinalizador DT_SET_IMMEDIATE do controle está definido. Para controles sem o DT_SET_IMMEDIATE sinalizador definido, as alterações nas propriedades são salvas quando o usuário descarte a caixa de diálogo clicando no botão **Okey** ou **Aplicar agora** . Quando um desses botões ou o botão **Cancelar** é clicado, MAPI remove a folha de propriedades da exibição. 
  
MAPI obtém acesso à sua tabela de exibição chamando o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) na implementação **IMAPIProp** e solicitar a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) ou herdando-lo em um chamadas feitas para MAPI, como [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).
  
A primeira técnica de acesso é usada quando os provedores de catálogo de endereços serão solicitadas que deseja mostrar detalhes sobre as mensagens de usuários ou listas de distribuição. O processamento seguinte ocorre:
  
1. Um cliente chama o método [IAddrBook::Details](iaddrbook-details.md) . 
    
2. MAPI chama o método de [IABLogon::OpenEntry](iablogon-openentry.md) do provedor catálogo de endereços para acessar o usuário de mensagens que representa a entrada selecionada. 
    
3. MAPI chama o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de mensagens do usuário para recuperar a propriedade **PR_DETAILS_TABLE** , a tabela de exibição para a caixa de diálogo detalhes. 
    
4. MAPI exibe a caixa de diálogo tratando a interação do usuário com as informações e remove-lo quando o usuário tiver terminado. 
    
## <a name="see-also"></a>Confira também



[Provedores de serviços MAPI](mapi-service-providers.md)

