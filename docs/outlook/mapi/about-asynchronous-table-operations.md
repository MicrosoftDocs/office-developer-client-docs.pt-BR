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
ms.openlocfilehash: 99bff153d4ce4bac3f85e0ed0feeaffafa6bf3f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766087"
---
# <a name="about-asynchronous-table-operations"></a>Sobre as operações de tabela assíncrona
 
**Aplica-se a**: Outlook 
  
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

