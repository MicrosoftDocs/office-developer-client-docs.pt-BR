---
title: Sobre as operações de tabela assíncrona
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1c31045e1fc19da63a2d4b61d92b3629afc96a55
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569409"
---
# <a name="about-asynchronous-table-operations"></a>Sobre as operações de tabela assíncrona
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A interface de **IMAPITable** inclui três métodos que operam de forma assíncrona e três métodos para controlar uma operação assíncrona. A tabela a seguir lista esses métodos: 
  
|**Operação assíncrona**|**Método de controle assíncrono**|
|:-----|:-----|
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |[IMAPITable::GetStatus](imapitable-getstatus.md) <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |[IMAPITable::Abort](imapitable-abort.md) <br/> |
|[IMAPITable::SortTable](imapitable-sorttable.md) <br/> |[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) <br/> |
   
**Para recuperar informações de status sobre o tipo e a operação atual de uma tabela**
  
- Chame [IMAPITable::GetStatus](imapitable-getstatus.md). Com **GetStatus**, um usuário de tabela pode determinar se a tabela é estático ou dinâmico, se uma operação está em andamento ou foi concluída e se ocorreu um erro de uma operação concluída. Por exemplo, se um cliente precisar cancelar uma operação de classificação, porque ele está demorando muito tempo, o cliente pode chamar primeiro **GetStatus** para determinar se, na verdade, uma operação de classificação está atualmente processando. Em seguida, o cliente pode chamar [IMAPITable::Abort](imapitable-abort.md) para interrompê-lo. 
    
**Para suspender atividade até que uma tarefa assíncrona seja concluída**
  
- Chame [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md). Chamar **WaitForCompletion** permite que a tarefa seja concluída sem interrupção. 
    
## <a name="see-also"></a>Confira também

- [Tabelas MAPI](mapi-tables.md)

