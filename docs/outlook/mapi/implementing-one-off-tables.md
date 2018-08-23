---
title: Implementar tabelas únicas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57933d44-d47a-4e7f-ba95-b49b4934d0a5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b86ec02c0255d892c42a9be9610d31b76041822c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579106"
---
# <a name="implementing-one-off-tables"></a>Implementar tabelas únicas

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Seu provedor pode implementar uma ou mais tabelas únicas. Uma tabela único é uma lista resumida de únicos modelos usados para criar os destinatários, diretamente em um contêiner ou para a lista de destinatários de uma mensagem de saída. Um modelo único é um utilizam de usuários do formulário para inserir dados relevantes para um determinado tipo de endereço. Quando o usuário estiver concluído trabalhar com o modelo, seu provedor cria o novo destinatário e o adiciona à mensagem. Geralmente cada modelo lida com um tipo de endereço único. No entanto, é possível para um modelo de lidar com vários tipos de ou para vários modelos de lidar com o mesmo tipo. 
  
Seu provedor deve suportar o método **OpenEntry** para cada modelo que inclui a tabela únicos. A implementação do **OpenEntry** deve recuperar de uma tabela de exibição para o modelo. MAPI usa a tabela de exibição para tornar o modelo visível para o usuário. 
  
Embora a maioria das linhas em tabelas únicas representa modelos, algumas das linhas podem ser usadas para categorizar ou agrupar os modelos. Representa uma linha em uma tabela único ou não um modelo é indicado pelo valor de uma coluna **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)). Linhas que representam os modelos de tem uma coluna PR_SELECTABLE definida como TRUE; linhas que representam modelos não tenham definido como FALSE.
  
MAPI define três tipos de tabelas únicos:
  
- Uma tabela único que reflete a modelos que oferece suporte a um contêiner individual
    
- Uma tabela único que reflete a todos os modelos que o provedor oferece suporte 
    
- Uma tabela único que reflete a todos os modelos que todos os provedores no perfil suportam plus alguns que oferece suporte a MAPI
    
Os dois primeiros tipos são implementados por provedores que suportam os destinatários de criação, em uma mensagem ou em um contêiner. Seu provedor pode incluir o mesmo conjunto ou um conjunto diferente de modelos em suas tabelas únicas. A principal diferença entre os dois tipos é que a tabela de provedor deve incluir modelos para criação de destinatários que podem ser usados em mensagens de saída e a tabela de contêiner deve incluir modelos para criação de destinatários a ser adicionado ao seu contêiner. Um contêiner pode oferecer suporte apenas a um conjunto restrito de modelos, mas a tabela únicos do provedor deve incluir a cada modelo o provedor oferece suporte.
  
O terceiro tipo de tabela único é implementado por MAPI; provedores de obtém acesso a ele chamando [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md). A tabela MAPI único é a união de todas as tabelas de provedor; Ela inclui cada modelo compatíveis com cada provedor no perfil. Ele também inclui modelos compatíveis com MAPI. Seu provedor pode usar essa tabela no lugar a tabela solicitada para um contêiner. No entanto, os modelos nesta tabela também podem ser usados para a criação de destinatários das mensagens de saída.
  

