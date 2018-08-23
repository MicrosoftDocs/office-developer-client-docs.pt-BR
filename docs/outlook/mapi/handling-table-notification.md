---
title: Manipulação de notificação de tabela
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b36e4697bfd4360f4ea6ea47c70eaaae434696d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595129"
---
# <a name="handling-table-notification"></a>Manipulação de notificação de tabela

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Como uma alternativa para registrar-se diretamente com um objeto de origem de advise, como uma pasta ou um usuário de mensagens, um cliente pode registrar para notificações sobre um conteúdo ou tabela de hierarquia. Controle de alterações endereço livro entradas, pastas e mensagens por meio de um conteúdo ou tabela de hierarquia pode ser mais simples e mais simples do que por meio de objetos individuais. 

Por exemplo, você pode chamar [IMAPITable::Advise](imapitable-advise.md) na tabela de hierarquia de uma pasta para descobrir quando as alterações ocorrem para uma de suas subpastas. Caso você ofereça suporte à exibição de mensagens remotas, registre-se com a tabela de status a serem observadas atividade por provedores de transporte e o spooler MAPI. 
  
No entanto, não é sempre preferível usar notificações de tabela, em vez de notificações de objeto. Monitoramento das alterações no número de mensagens em uma pasta é um exemplo de quando seu cliente talvez precisem registrar para notificações do objeto em uma pasta, e não em uma tabela implementadas pela pasta.
  

