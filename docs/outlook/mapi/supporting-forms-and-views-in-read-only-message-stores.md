---
title: Suporte a formulários e modos de exibição em repositórios de mensagens somente leitura
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da5f080d-4397-4ce6-8561-73dd13445e77
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1ef9b85fd8dad980f92f5e06a4b54daf146fbcec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770536"
---
# <a name="supporting-forms-and-views-in-read-only-message-stores"></a>Suporte a formulários e modos de exibição em repositórios de mensagens somente leitura

  
  
**Aplica-se a**: Outlook 
  
Se seu provedor de armazenamento de mensagens permite que a permissão somente leitura para o mecanismo de armazenamento subjacente, os aplicativos cliente e o Gerenciador de formulário MAPI poderão realizar certas tarefas. Especificamente, os clientes não poderão adicionar ou modificar modos de exibição personalizados e o Gerenciador de formulário MAPI poderão instalar formulários nas tabelas de pastas do repositório de conteúdo associado.
  
Para muitos repositórios de mensagem de somente leitura, que pode não ser um problema. Se for esse o caso, o provedor de armazenamento de mensagem não precisa oferecer suporte a tabelas de conteúdo associado nisso. No entanto, se seu provedor de armazenamento de mensagem deve ser somente leitura e ele também deve oferecer suporte a um conjunto predefinido de formulários ou modos de exibição, será necessário dar suporte a tabelas de conteúdo associado.
  
A estratégia mais comuns para fazer isso, porque os clientes e o Gerenciador de formulário MAPI não é possível instalar os modos de exibição ou formulários na mensagem armazenam sozinhos, é para o provedor de armazenamento de mensagem codificá--los para o repositório de mensagem. Isso significa que a tabela de conteúdo associados ou tabelas que contêm os modos de exibição ou formulários continuará a existir no repositório de mensagem quando ele é criado, antes de todos os clientes ou MAPI Gerenciador de formulário nunca acessá-lo. Em seguida, quando um cliente solicitar uma tabela de conteúdo associado ao fazer exibições personalizadas a partir de um formulário ou o Gerenciador de formulário MAPI solicita uma tabela de conteúdo associado à inicialização de um formulário, o provedor de armazenamento de mensagens pode fornecer uma. 
  
Esse requisito que as tabelas de conteúdo associado deve ser criadas e preenchidas quando o armazenamento de mensagens em si é criado indica que o seu provedor de armazenamento de mensagem precisará obter informações sobre o formato das mensagens especiais que clientes e o formulário MAPI Gerenciador de usar para armazenar os modos de exibição e formulários. Cite empregar esses formatos dependerá o cliente e o Gerenciador de formulário MAPI que está sendo usado, portanto, uma descrição que eles não pode ser fornecida aqui.
  
## <a name="see-also"></a>Confira também



[Repositórios de mensagens somente leitura](read-only-message-stores.md)

