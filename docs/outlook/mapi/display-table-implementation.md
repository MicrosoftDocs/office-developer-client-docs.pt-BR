---
title: Exibir a implementação da tabela
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
# <a name="display-table-implementation"></a>Exibir a implementação da tabela

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela de exibição é usada para mostrar uma folha de propriedades, uma caixa de diálogo especial que é composta de uma ou mais páginas de propriedades com guias dedicadas para exibir e possivelmente editar uma ou mais propriedades. Associado a cada tabela de exibição é uma implementação de interface [IAttach: IMAPIProp](iattachimapiprop.md) . A implementação do [IMAPIProp](imapipropiunknown.md) mantém os dados de propriedade apresentados na folha de propriedades. 
  
As linhas em uma tabela de exibição representam os controles na folha de propriedades. A maioria dos controles pode ser associada às propriedades mantidas com a implementação **IMAPIProp** . Quando um usuário altera o valor de um controle modificável, a propriedade correspondente é atualizada. 
  
As colunas em uma tabela de exibição representam as propriedades do controle, como sua posição na folha de propriedades, o tipo, a estrutura associada e o identificador. Para obter uma lista completa das colunas de exibição obrigatórias da tabela, confira [Exibir tabelas](display-tables.md).
  
MAPI exibe uma folha de propriedades para o usuário de um aplicativo cliente lendo valores de propriedade da implementação **IMAPIProp** associada à tabela de exibição ou a partir da tabela de exibição diretamente. Como o usuário trabalha com a folha de propriedades, alterando os valores nos controles, MAPI chama [IMAPIProp::](imapiprop-setprops.md) SetProps para salvar um controle alterado se o sinalizador DT_SET_IMMEDIATE do controle estiver definido. Para controles sem o sinalizador DT_SET_IMMEDIATE definido, as alterações nas propriedades são salvas quando o usuário ignora a caixa de diálogo clicando no botão **OK** ou **aplicar agora** . Quando um desses botões ou o botão **Cancelar** é clicado, MAPI remove a folha de propriedades do modo de exibição. 
  
O MAPI obtém acesso à sua tabela de exibição chamando o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) na implementação **IMAPIProp** e solicitando a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) ou herdando-a em um chamada que você fez para MAPI, como [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md).
  
A primeira técnica de acesso é usada quando os provedores de catálogos de endereços são solicitados a mostrar detalhes sobre usuários de mensagens ou listas de distribuição. O seguinte processamento ocorre:
  
1. Um cliente chama o método [IAddrBook::D etails](iaddrbook-details.md) . 
    
2. MAPI chama o método [IABLogon:: OpenEntry](iablogon-openentry.md) do provedor de catálogo de endereços para acessar o usuário de mensagens que representa a entrada selecionada. 
    
3. MAPI chama o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) do usuário de mensagens para recuperar a propriedade **PR_DETAILS_TABLE** , a tabela de exibição da caixa de diálogo detalhes. 
    
4. MAPI exibe a caixa de diálogo, manipulando a interação do usuário com as informações e a remove quando o usuário tiver concluído. 
    
## <a name="see-also"></a>Confira também



[Provedores de serviço MAPI](mapi-service-providers.md)

