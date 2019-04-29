---
title: Sobre operações de tabela assíncronas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: eebc04e2263b4a2037e167bd464a31d298b84664
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439566"
---
# <a name="about-asynchronous-table-operations"></a>Sobre operações de tabela assíncronas
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A **** interface IMAPITable inclui três métodos que operam de forma assíncrona e três métodos para controlar uma operação assíncrona. A tabela a seguir lista esses métodos: 
  
|**Operação asSíncrona**|**Método de controle assíncrono**|
|:-----|:-----|
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |[IMAPITable::GetStatus](imapitable-getstatus.md) <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |[IMAPITable::Abort](imapitable-abort.md) <br/> |
|[IMAPITable::SortTable](imapitable-sorttable.md) <br/> |[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) <br/> |
   
**Para recuperar as informações de status sobre o tipo de tabela e a operação atual**
  
- Call [IMAPITable:: GetStatus](imapitable-getstatus.md). Com **GetStatus**, um usuário de tabela pode determinar se a tabela é estática ou dinâmica, se uma operação estiver em andamento ou tiver sido concluída e se um erro ocorreu de uma operação concluída. Por exemplo, se um cliente precisa cancelar uma operação de classificação porque está demorando muito tempo, o cliente pode primeiro chamar **GetStatus** para determinar se, na verdade, uma operação de classificação está sendo processada no momento. Em seguida, o cliente pode chamar imApitable [:: Abort](imapitable-abort.md) para interrompê-lo. 
    
**Para suspender a atividade até que uma tarefa assíncrona tenha sido concluída**
  
- Call [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md). Chamar **WaitForCompletion** permite que a tarefa seja concluída sem interrupção. 
    
## <a name="see-also"></a>Confira também

- [Tabelas MAPI](mapi-tables.md)

