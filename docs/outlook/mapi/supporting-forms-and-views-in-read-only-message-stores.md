---
title: Suporte a formulários e modos de exibição em repositórios de mensagens somente leitura
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da5f080d-4397-4ce6-8561-73dd13445e77
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 0b7ffe07278cfcbba95351f2720e427dd8500221
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350614"
---
# <a name="supporting-forms-and-views-in-read-only-message-stores"></a>Suporte a formulários e modos de exibição em repositórios de mensagens somente leitura

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se o seu provedor de repositório de mensagens permitir a permissão somente leitura para o mecanismo de armazenamento subjacente, os aplicativos cliente e o Gerenciador de formulários MAPI não poderão realizar certas coisas. Especificamente, os clientes não poderão adicionar ou modificar modos de exibição personalizados, e o Gerenciador de formulários MAPI não poderá instalar formulários nas tabelas de conteúdo associadas das pastas do repositório.
  
Para muitos repositórios de mensagens somente leitura, isso pode não ser um problema. Se esse for o caso, o provedor do repositório de mensagens não precisará dar suporte a tabelas de conteúdo associado. No enTanto, se o seu provedor de repositório de mensagens deve ser somente leitura e também deve oferecer suporte a um conjunto predefinido de modos de exibição ou formulários, ele precisará suportar tabelas de conteúdo associado.
  
A estratégia mais comum para fazer isso, porque os clientes e o Gerenciador de formulários MAPI não podem instalar os modos de exibição ou formulários no repositório de mensagens, são para o provedor de repositórios de mensagens para embutir o código no repositório de mensagens. Isso significa que a tabela de conteúdo associada ou as tabelas que contêm os modos de exibição ou formulários existirão no repositório de mensagens quando ele for criado, antes de qualquer cliente ou o Gerenciador de formulários MAPI, acessando-o. Em seguida, quando um cliente solicita uma tabela de conteúdo associado para obter modos de exibição personalizados de um formulário ou o Gerenciador de formulários MAPI solicita uma tabela de conteúdo associada para iniciar um formulário, o provedor de repositório de mensagens pode fornecer um. 
  
Esse requisito de que as tabelas de conteúdo associadas sejam criadas e preenchidas quando o próprio repositório de mensagens é criado implica que seu provedor de repositório de mensagens precisará obter informações sobre o formato das mensagens especiais que os clientes e o formulário MAPI Manager use para armazenar modos de exibição e formulários. O que esses formatos irão depender do cliente e do Gerenciador de formulários MAPI sendo usados, portanto, uma descrição deles não pode ser fornecida aqui.
  
## <a name="see-also"></a>Confira também



[Repositórios de mensagens somente leitura](read-only-message-stores.md)

