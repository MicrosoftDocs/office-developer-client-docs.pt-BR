---
title: Implementando One-Off tabelas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57933d44-d47a-4e7f-ba95-b49b4934d0a5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c29feae84d81874988997409fd229b042a701640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421638"
---
# <a name="implementing-one-off-tables"></a>Implementando tabelas One-Off tabelas

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Seu provedor pode implementar uma ou mais tabelas one-off. Uma tabela única é uma lista resumida de modelos one-off usados para criar destinatários, diretamente em um contêiner ou na lista de destinatários de uma mensagem de saída. Um modelo único é um formulário que os usuários empregam para inserir dados relevantes para um tipo específico de endereço. Quando o usuário terminar de trabalhar com o modelo, o provedor criará o novo destinatário e o adiciona à mensagem. Normalmente, cada modelo lida com um único tipo de endereço. No entanto, é possível que um modelo manipular vários tipos ou vários modelos manipular o mesmo tipo. 
  
Seu provedor deve dar suporte **ao método OpenEntry** para cada modelo que ele inclui na tabela única. A implementação de **OpenEntry** deve recuperar uma tabela de exibição para o modelo. O MAPI usa a tabela de exibição para tornar o modelo visível para o usuário. 
  
Embora a maioria das linhas em tabelas um-off represente modelos, algumas das linhas podem ser usadas para categorizar, ou agrupar, modelos. Se uma linha em uma tabela única representa ou não um modelo é indicado pelo valor de sua **coluna PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)). As linhas que representam modelos têm a PR_SELECTABLE coluna definida como TRUE; linhas que não representam modelos a têm definida como FALSE.
  
MAPI define três tipos de tabelas one-off:
  
- Uma tabela única que reflete os modelos compatíveis com um contêiner individual
    
- Uma tabela única que reflete todos os modelos compatíveis com seu provedor 
    
- Uma tabela única que reflete todos os modelos que todos os provedores no perfil suportam, além de alguns que o MAPI suporta
    
Os dois primeiros tipos são implementados por provedores que suportam os destinatários de criação, em uma mensagem ou em um contêiner. Seu provedor pode incluir o mesmo conjunto ou um conjunto diferente de modelos em suas tabelas one-off. A principal diferença entre os dois tipos é que sua tabela de provedor deve incluir modelos para a criação de destinatários que podem ser usados em mensagens de saída e sua tabela de contêineres deve incluir modelos para a criação de destinatários a serem adicionados ao contêiner. Um contêiner só pode dar suporte a um conjunto restrito de modelos, mas a tabela única do provedor deve incluir todos os modelos compatíveis com o provedor.
  
O terceiro tipo de tabela única é implementado pelo MAPI; os provedores têm acesso a ele chamando [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md). A tabela única MAPI é a união de todas as tabelas de provedores; ele inclui todos os modelos suportados por todos os provedores no perfil. Ele também inclui modelos com suporte pela MAPI. Seu provedor pode usar essa tabela no lugar da tabela solicitada para um contêiner. No entanto, os modelos nesta tabela também podem ser usados para criar destinatários para mensagens de saída.
  

