---
title: Manipular notificações de tabela
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6e6c24c3836f295054c1880dc506c5051078a9ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435891"
---
# <a name="handling-table-notification"></a>Manipular notificações de tabela

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Como alternativa ao registro direto com um objeto de origem de aviso, como uma pasta ou um usuário de mensagens, um cliente pode se registrar para notificações em uma tabela de conteúdo ou hierarquia. Controlar alterações em entradas do catálogo de endereços, pastas e mensagens por meio de uma tabela de conteúdo ou hierarquia pode ser mais simples e simples do que por objetos individuais. 

Por exemplo, você pode chamar [IMAPITable:: Advise](imapitable-advise.md) na tabela de hierarquia da pasta para descobrir quando as alterações ocorrem em uma de suas subpastas. Se você oferecer suporte à exibição de mensagens remotas, registre-se com a tabela de status para observar a atividade por provedores de transporte e pelo spooler MAPI. 
  
No enTanto, nem sempre é preferível usar as notificações de tabela em vez de notificações de objeto. O monitoramento de alterações no número de mensagens em uma pasta é um exemplo de quando o cliente pode precisar registrar notificações de objeto em uma pasta, em vez de em uma tabela implementada pela pasta.
  

