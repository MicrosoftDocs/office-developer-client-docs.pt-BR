---
title: Pastas especiais de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f2aa2376-b293-4d05-9104-218cc1fe1758
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 396a6c01d0b9cd867706a7dd4997bd6ddd7fd147
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578287"
---
# <a name="mapi-special-folders"></a>Pastas especiais de MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI define algumas pastas que são especiais porque eles atuam funções predefinidas como pastas padrão para determinados tipos de mensagens. Nessas pastas especiais geralmente não podem ser excluídas e têm propriedades do identificador de entrada especial.
  
Há oito pastas especiais, alguns que fazem parte da subárvore interpessoais mensagens (IPM). MAPI cria essas pastas antes que um cliente recebe acesso ao seu armazenamento de mensagens, após o qual o cliente pode ser capaz de excluir as pastas, se necessário. Alguns provedores de armazenamento de mensagens permitem a exclusão, enquanto outros não. A tabela a seguir descreve essas pastas.
  
**Pastas MAPI**

|**Folder**|**Descrição**|
|:-----|:-----|
|Pasta caixa de saída  <br/> |Contém mensagens de saída IPM.  <br/> |
|Pasta de itens excluídos  <br/> |Contém IPM mensagens marcadas para exclusão.  <br/> |
|Pasta Itens enviados  <br/> |Contém mensagens IPM que foram enviadas.  <br/> |
|Pasta de raiz IPM  <br/> |Contém pastas para gerenciamento de mensagens IPM.  <br/> |
|Pasta de recebimento  <br/> |Contém mensagens de entrada para uma classe de mensagem específica.  <br/> |
|Pasta raiz de resultados de pesquisa  <br/> |Contém pastas para gerenciar os resultados da pesquisa.  <br/> |
|Pasta de raiz comum modos de exibição  <br/> |Contém pastas para gerenciar modos de exibição para o armazenamento de mensagens.  <br/> |
|Pasta raiz de modos de exibição de pessoal  <br/> |Contém pastas para gerenciar modos de exibição para um usuário específico.  <br/> |
   
As primeiras quatro pastas se relacionam com a subárvore IPM, uma árvore de pastas MAPI cria quando um armazenamento de mensagens é inicializado. Repositórios de mensagem padrão para clientes de mensagens interativos sempre incluem subárvore IPM pasta e as outras pastas especiais na sua hierarquia de pastas. Repositórios de mensagem padrão não são necessárias somente para oferecer suporte a pasta raiz de resultados da pesquisa, a pasta de raiz subárvore IPM, a pasta Itens excluídos e a pasta de recebimento. Para garantir que as pastas de subárvore IPM existam e sejam válidas, os clientes podem chamar a função de [HrValidateIPMSubtree](hrvalidateipmsubtree.md) . **HrValidateIPMSubtree** verifica as pastas e os recria se houver um problema. 
  
As pastas raiz para os resultados da pesquisa, modos de exibição comuns e exibições pessoais não são parte da subárvore IPM; Essas pastas são criadas na pasta raiz para o armazenamento de mensagens. A pasta raiz de resultados de pesquisa contém pastas que oferecem suporte a tabelas de conteúdo com as mensagens que satisfazem um conjunto de critérios de pesquisa. Embora os clientes têm permissão para criar pastas de resultados de pesquisa em qualquer pasta, a maioria dos clientes designar uma pasta raiz única para ser o pai de todos os resultados de pesquisa pastas criadas durante a sessão. 
  
As pastas de raiz comum modos de exibição e pessoal contêm mensagens que descrevem os modos de exibição ou preferenciais maneiras de apresentar os dados de mensagens e pastas. Pasta raiz comum modos de exibição contém modos de exibição que os clientes podem ser usados com qualquer pasta no repositório de mensagem; a pasta de modos de exibição de pessoal contém modos de exibição que foram definidos por um usuário específico para uma pasta particular ou pastas.
  
Os clientes que funcionam com mensagens IPM devem criar todas as pastas e mensagens sob a pasta de raiz subárvore IPM, em vez da pasta raiz do armazenamento de mensagens. Isso dá aos clientes não-IPM — os clientes que lidam com mensagens trocadas entre computadores ou entre as pessoas e computadores — uma maneira fácil para ocultar suas mensagens de clientes IPM. 
  
MAPI atribui a entrada especial propriedades de identificador para essas pastas especiais. Para obter uma lista dos identificadores de entrada de pasta especial, consulte [abrindo uma pasta de repositório de mensagem](opening-a-message-store-folder.md).
  
### <a name="outlook-special-folders"></a>Pastas especiais do Outlook

Pastas especiais do Outlook são identificadas por seu IDs que estão armazenados na pasta caixa de entrada e a pasta raiz para o armazenamento de mensagens de entrada.
  
|**Folder**|**Para definir a propriedade**|
|:-----|:-----|
|Calendário  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Contatos  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Diário  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Observações  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Tarefas  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
|Rascunhos  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Confira também



[Pastas MAPI](mapi-folders.md)

