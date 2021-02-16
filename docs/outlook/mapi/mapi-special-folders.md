---
title: Pastas especiais MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f2aa2376-b293-4d05-9104-218cc1fe1758
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fa221510a5f6a8c8be24b4869960d1770cef5882
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410921"
---
# <a name="mapi-special-folders"></a>Pastas especiais MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI define algumas pastas que são especiais porque elas servem funções predefinidos como pastas padrão para determinados tipos de mensagens. Essas pastas especiais normalmente não podem ser excluídas e têm propriedades de identificador de entrada especiais.
  
Há oito pastas especiais, algumas que fazem parte da subárvore de mensagem interpersonal (IPM). O MAPI cria essas pastas antes que um cliente receba acesso ao seu armazenamento de mensagens, após o qual o cliente poderá excluir as pastas, se necessário. Alguns provedores de armazenamento de mensagens permitem a exclusão, enquanto outros não. A tabela a seguir descreve essas pastas.
  
**Pastas MAPI**

|**Folder**|**Descrição**|
|:-----|:-----|
|Pasta caixa de saída  <br/> |Contém mensagens IPM de saída.  <br/> |
|pasta Itens Excluídos  <br/> |Contém mensagens IPM marcadas para exclusão.  <br/> |
|Pasta Itens Enviados  <br/> |Contém mensagens IPM que foram enviadas.  <br/> |
|Pasta raiz do IPM  <br/> |Contém pastas para gerenciar mensagens IPM.  <br/> |
|Pasta de recebimento  <br/> |Contém mensagens de entrada para uma classe de mensagem específica.  <br/> |
|Pasta raiz de resultados de pesquisa  <br/> |Contém pastas para gerenciar resultados de pesquisa.  <br/> |
|Pasta raiz de exibições comuns  <br/> |Contém pastas para gerenciar exibições para o armazenamento de mensagens.  <br/> |
|Pasta raiz de exibições pessoais  <br/> |Contém pastas para gerenciar exibições de um usuário específico.  <br/> |
   
As quatro primeiras pastas estão relacionadas à subárvore do IPM, uma árvore de pastas que o MAPI cria quando um armazenamento de mensagens é inicializado. Os armazenamentos de mensagens padrão para clientes de mensagens interativas sempre incluem a subárvore da pasta do IPM e outras pastas especiais em sua hierarquia de pastas. Os armazenamentos de mensagens não padrão são necessários apenas para dar suporte à pasta raiz de resultados de pesquisa, à pasta raiz da subárvore do IPM, à pasta Itens Excluídos e à pasta de recebimento. Para garantir que as pastas de subárvore do IPM existam e sejam válidas, os clientes podem chamar [a função HrValidateIPMSubtree.](hrvalidateipmsubtree.md) **HrValidateIPMSubtree** verifica as pastas e as recria se houver um problema. 
  
As pastas raiz para resultados de pesquisa, exibições comuns e exibições pessoais não fazem parte da subárvore do IPM; essas pastas são criadas na pasta raiz do armazenamento de mensagens. A pasta raiz de resultados de pesquisa contém pastas que suportam tabelas de conteúdo com mensagens que atendam a um conjunto de critérios de pesquisa. Embora os clientes tenham permissão para criar pastas de resultados de pesquisa em qualquer pasta, a maioria dos clientes designa uma única pasta raiz para ser pai de todas as pastas de resultados de pesquisa criadas durante a sessão. 
  
As pastas raiz de modos de exibição comuns e de modos de exibição pessoais contêm mensagens que descrevem modos de exibição ou maneiras preferenciais de apresentar dados de mensagens e pastas. A pasta raiz de exibições comuns contém exibições que os clientes podem usar com qualquer pasta no armazenamento de mensagens; a pasta de exibições pessoais contém exibições que foram definidas por um usuário específico para uma determinada pasta ou pastas.
  
Os clientes que trabalham com mensagens IPM devem criar todas as pastas e mensagens sob a pasta raiz da subárvore do IPM, em vez da pasta raiz do armazenamento de mensagens. Isso oferece aos clientes que não são do IPM — os clientes que lidam com mensagens trocadas entre computadores ou entre humanos e computadores — uma maneira fácil de ocultar suas mensagens de clientes IPM. 
  
MAPI assigns special entry identifier properties for these special folders. Para uma lista dos identificadores de entrada de pasta especial, consulte [Abrindo uma pasta do armazenamento de mensagens.](opening-a-message-store-folder.md)
  
### <a name="outlook-special-folders"></a>Pastas Especiais do Outlook

As pastas especiais do Outlook são identificadas por suas IDs de entrada armazenadas na pasta Caixa de Entrada e na pasta raiz do armazenamento de mensagens.
  
|**Folder**|**A propriedade a ser definida**|
|:-----|:-----|
|Calendário  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Contatos  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Diário  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Observações  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Tarefas  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
|Rascunhos  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Confira também



[Pastas MAPI](mapi-folders.md)

