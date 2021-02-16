---
title: Suporte a formulários e exibições em Read-Only de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da5f080d-4397-4ce6-8561-73dd13445e77
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 0b7ffe07278cfcbba95351f2720e427dd8500221
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432426"
---
# <a name="supporting-forms-and-views-in-read-only-message-stores"></a>Suporte a formulários e exibições em Read-Only de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se seu provedor de armazenamento de mensagens permitir permissão somente leitura para o mecanismo de armazenamento subjacente, os aplicativos cliente e o gerenciador de formulário MAPI não poderão fazer determinadas coisas. Especificamente, os clientes não poderão adicionar ou modificar exibições personalizadas, e o gerenciador de formulários MAPI não poderá instalar formulários nas tabelas de conteúdo associadas das pastas do armazenamento.
  
Para muitos armazenamentos de mensagens somente leitura, isso pode não ser um problema. Se esse for o caso, o provedor de armazenamento de mensagens não precisa dar suporte a tabelas de conteúdo associadas. No entanto, se seu provedor de armazenamento de mensagens deve ser somente leitura e também deve suportar um conjunto predefinido de exibições ou formulários, ele precisará dar suporte a tabelas de conteúdo associadas.
  
A estratégia mais comum para fazer isso, porque os clientes e o gerenciador de formulários MAPI não podem instalar os próprios formulários ou exibições no armazenamento de mensagens, é que o provedor de armazenamento de mensagens os codifica no armazenamento de mensagens. Isso significa que a tabela ou tabelas de conteúdo associadas que contêm os formulários ou exibições existirão no armazenamento de mensagens quando ele for criado, antes de qualquer cliente ou o gerenciador de formulários MAPI acessá-lo. Em seguida, quando um cliente solicita uma tabela de conteúdo associada para obter exibições personalizadas de um formulário ou o gerenciador de formulário MAPI solicita uma tabela de conteúdo associada para iniciar um formulário, o provedor de armazenamento de mensagens pode fornecer um. 
  
Esse requisito de que as tabelas de conteúdo associadas sejam criadas e preenchidas quando o próprio armazenamento de mensagens for criado implica em que seu provedor de armazenamento de mensagens precisará obter informações sobre o formato das mensagens especiais que os clientes e o gerenciador de formulários MAPI usam para armazenar exibições e formulários. O uso desses formatos dependerá do cliente e do gerenciador de formulário MAPI, portanto, uma descrição deles não pode ser fornecida aqui.
  
## <a name="see-also"></a>Confira também



[Armazenamentos de Mensagens Somente Leitura](read-only-message-stores.md)

