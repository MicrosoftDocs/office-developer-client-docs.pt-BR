---
title: Implementar tabelas únicas
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
# <a name="implementing-one-off-tables"></a>Implementar tabelas únicas

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O provedor pode implementar uma ou mais tabelas únicas. Uma tabela única é uma lista resumida de modelos únicos usados para criar destinatários, diretamente para um contêiner ou para a lista de destinatários de uma mensagem de saída. Um modelo one-off é um formulário que os usuários empregam para inserir dados relevantes para um determinado tipo de endereço. Quando o usuário termina de trabalhar com o modelo, seu provedor cria o novo destinatário e o adiciona à mensagem. Normalmente, cada modelo trata de um único tipo de endereço. No enTanto, é possível que um modelo manipule vários tipos ou vários modelos para lidar com o mesmo tipo. 
  
Seu provedor deve oferecer suporte ao método **OpenEntry** para cada modelo que ele inclui na tabela one-off. A implementação do **OpenEntry** deve recuperar uma tabela de exibição do modelo. MAPI usa a tabela de exibição para tornar o modelo visível para o usuário. 
  
Embora a maioria das linhas em tabelas únicas representem modelos, algumas das linhas podem ser usadas para categorizar ou agrupar modelos. Se uma linha de uma tabela única representa ou não um modelo é indicada pelo valor de sua coluna **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)). As linhas que representam modelos têm a coluna PR_SELECTABLE definida como TRUE; as linhas que não representam modelos foram definidas como FALSE.
  
MAPI define três tipos de tabelas únicas:
  
- Uma tabela única que reflete os modelos aos quais um contêiner individual oferece suporte
    
- Uma tabela única que reflete todos os modelos aos quais o provedor oferece suporte 
    
- Uma tabela única que reflete todos os modelos de que todos os provedores no perfil dão suporte, mais algumas de suporte a MAPI
    
Os dois primeiros tipos são implementados por provedores que dão suporte aos destinatários de criação, em uma mensagem ou em um contêiner. O provedor pode incluir o mesmo conjunto ou um conjunto diferente de modelos em suas tabelas únicas. A principal diferença entre os dois tipos é que sua tabela de provedor deve incluir modelos para a criação de destinatários que podem ser usados em mensagens de saída e sua tabela de contêiner deve incluir modelos para a criação de destinatários a serem adicionados ao seu contêiner. Um contêiner só pode dar suporte a um conjunto restrito de modelos, mas a tabela única do provedor deve incluir todos os modelos que o provedor suporta.
  
O terceiro tipo de tabela única é implementado por MAPI; os provedores obtêm acesso a ele chamando [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md). A tabela única de MAPI é a União de todas as tabelas de provedor; Ele inclui todos os modelos suportados por todos os provedores no perfil. Também inclui modelos suportados por MAPI. O provedor pode usar essa tabela no lugar da tabela solicitada para um contêiner. No enTanto, os modelos nesta tabela também podem ser usados para criar destinatários para mensagens de saída.
  

