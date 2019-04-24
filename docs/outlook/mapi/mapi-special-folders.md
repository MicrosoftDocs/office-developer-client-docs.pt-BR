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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357355"
---
# <a name="mapi-special-folders"></a>Pastas especiais MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI define algumas pastas que são especiais porque servem funções predefinidas como pastas padrão para determinados tipos de mensagens. Essas pastas especiais normalmente não podem ser excluídas e têm propriedades de identificador de entrada especiais.
  
Há oito pastas especiais, algumas que fazem parte da sub-árvore da mensagem interpessoal (IPM). O MAPI cria essas pastas antes de um cliente receber acesso ao repositório de mensagens, após o qual o cliente poderá excluir as pastas, se necessário. Alguns provedores de repositórios de mensagens permitem exclusão, enquanto outros não. A tabela a seguir descreve essas pastas.
  
**Pastas MAPI**

|**Folder**|**Descrição**|
|:-----|:-----|
|Pasta de saída  <br/> |Contém mensagens de saída IPM.  <br/> |
|pasta Itens Excluídos  <br/> |Contém mensagens IPM marcadas para exclusão.  <br/> |
|Pasta Itens enviados  <br/> |Contém mensagens IPM que foram enviadas.  <br/> |
|Pasta raiz IPM  <br/> |Contém pastas para o gerenciamento de mensagens IPM.  <br/> |
|Pasta receber  <br/> |Contém mensagens de entrada para uma determinada classe de mensagem.  <br/> |
|Pasta raiz de resultados de pesquisa  <br/> |Contém pastas para gerenciar resultados de pesquisa.  <br/> |
|Common – pasta raiz de modos de exibição  <br/> |Contém pastas para gerenciar modos de exibição para o repositório de mensagens.  <br/> |
|Pasta raiz de exibições pessoais  <br/> |Contém pastas para o gerenciamento de modos de exibição para um usuário específico.  <br/> |
   
As quatro primeiras pastas se relacionam com a sub-árvore IPM, uma árvore de pastas que o MAPI cria quando um repositório de mensagens é inicializado. Os repositórios de mensagens padrão para clientes de mensagens interativas sempre incluem a subárvore de pastas IPM e as outras pastas especiais em sua hierarquia de pastas. Os repositórios de mensagens não padrão são necessários apenas para oferecer suporte à pasta raiz de resultados de pesquisa, à pasta raiz de sub-árvore IPM, à pasta itens excluídos e à pasta receber. Para garantir que as pastas de sub-árvore IPM existam e sejam válidas, os clientes podem chamar a função [HrValidateIPMSubtree](hrvalidateipmsubtree.md) . **HrValidateIPMSubtree** verifica as pastas e as recria se houver um problema. 
  
As pastas raiz dos resultados de pesquisa, modos de exibição comuns e modos de exibição pessoais não fazem parte da sub-árvore IPM; essas pastas são criadas na pasta raiz do repositório de mensagens. A pasta raiz de resultados de pesquisa contém pastas que dão suporte a tabelas de conteúdo com mensagens que atendem a um conjunto de critérios de pesquisa. Embora os clientes tenham permissão para criar pastas de resultados de pesquisa em qualquer pasta, a maioria dos clientes designa uma única pasta raiz como pai de todas as pastas de resultados de pesquisa criadas durante a sessão. 
  
As pastas raiz de modos de exibição pessoais e modos de exibição pessoais contêm mensagens que descrevem modos de exibição ou maneiras preferidas de apresentar dados de mensagens e pastas. A pasta raiz de modos de exibição comuns contém modos de exibição que os clientes podem usar com qualquer pasta no repositório de mensagens; a pasta de modos de exibição pessoais contém modos de exibição que foram definidos por um usuário específico para uma ou mais pastas específicas.
  
Os clientes que trabalham com mensagens IPM devem criar todas as pastas e mensagens na pasta raiz da sub-árvore IPM, e não na pasta raiz do repositório de mensagens. Isso fornece clientes não-IPM, os clientes que lidam com mensagens trocadas entre computadores ou entre seres humanos e computadores, uma maneira fácil de ocultar suas mensagens de clientes IPM. 
  
MAPI atribui Propriedades de identificador de entrada especiais para essas pastas especiais. Para obter uma lista dos identificadores de entrada de pasta especial, confira [abrir uma pasta de repositório de mensagens](opening-a-message-store-folder.md).
  
### <a name="outlook-special-folders"></a>Pastas especiais do Outlook

As pastas especiais do Outlook são identificadas por suas IDs de entrada que são armazenadas na pasta caixa de entrada e na pasta raiz do repositório de mensagens.
  
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

