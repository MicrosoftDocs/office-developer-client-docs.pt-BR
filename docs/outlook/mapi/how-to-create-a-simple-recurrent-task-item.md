---
title: Criar um item de tarefa simples de recorrência
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e9ee8865-0983-439e-8405-7946c5ec8762
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: be765915b729824b8c8b4209f125f354b02bad2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345469"
---
# <a name="create-a-simple-recurrent-task-item"></a>Criar um item de tarefa simples de recorrência

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI pode ser usado para criar itens de tarefa. Este tópico descreve como criar um item de tarefa recorrente simples.
  
Para obter informações sobre como baixar, exibir e executar o código do aplicativo MFCMAPI e o projeto do CreateOutlookItemsAddin referenciado neste tópico, consulte [install the Samples Used in this section](how-to-install-the-samples-used-in-this-section.md).

### <a name="to-create-a-task-item"></a>Para criar um item de tarefa

1. Abra um repositório de mensagens. Para obter informações sobre como abrir um repositório de mensagens, consulte [abrir um repositório de mensagens](opening-a-message-store.md).
    
2. Abra a pasta tarefas no repositório de mensagens. Para obter mais informações, consulte **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).
    
3. Chame o método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) na pasta tarefas para criar o novo item de tarefa. 
    
4. Defina a propriedade **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) e outras propriedades relacionadas à tarefa necessárias para criar uma tarefa recorrente.
    
5. Salve o novo item de tarefa.
    
A `AddTask` função no arquivo de origem Tasks. cpp do projeto CreateOutlookItemsAddin demonstra essas etapas. A `AddTask` função usa parâmetros da caixa de diálogo **Adicionar tarefa** que é exibida quando você clica em **Adicionar tarefa** no menu **AddIns** no aplicativo de exemplo MFCMAPI. A `DisplayAddTaskDialog` função em Tasks. cpp exibe a caixa de diálogo e passa valores da caixa de diálogo para `AddTask` a função. A `DisplayAddTaskDialog` função não está relacionada diretamente à criação de um item de tarefa usando MAPI, portanto, não está listada aqui. 
  
> [!IMPORTANT]
> O código no aplicativo MFCMAPI não garante que a pasta **tarefas** tenha sido selecionada quando você clicar no comando **Adicionar tarefa** no menu AddIns **** . A criação de itens de tarefa em uma pasta diferente da pasta **tarefas** pode causar comportamento indefinido. Verifique se você selecionou a pasta **tarefas** antes de usar o comando **Adicionar tarefa** no aplicativo do MFCMAPI. 
  
A `AddTask` função está listada abaixo. Observe que o parâmetro _lpFolder_ passado para a `AddTask` função é um ponteiro para uma interface [IMAPIFolder](imapifolderimapicontainer.md) que representa a pasta na qual a nova tarefa é criada. Dada a _lpFolder_ que representa uma interface **IMAPIFolder** , o código chama o método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) . O **** Método CreateMessage retorna um código de êxito e um ponteiro para um ponteiro para uma interface **IMessage** . A maior parte `AddTask` do código de função trata do trabalho de especificação de propriedades em preparação para chamar o método [IMAPIProp::](imapiprop-setprops.md) SetProps. Se a chamada para o **** método SetProps for bem-sucedida, o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) será chamado para confirmar as alterações no repositório e criar um novo item de tarefa. 
  
A `AddTask` função define um número de propriedades nomeadas. Para obter informações sobre propriedades nomeadas e como elas são criadas, consulte [usando o MAPI para criar itens do Outlook 2007](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx). Como as propriedades nomeadas usadas para itens de tarefa ocupam vários conjuntos de propriedades, é necessário tomar cuidado ao criar parâmetros a serem passados para o método [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) . 
  
A `AddTask` função usa a `BuildWeeklyTaskRecurrencePattern` função auxiliar para criar uma estrutura que representa uma recorrência de tarefa para a configuração da propriedade **dispidTaskRecur** . Para obter informações sobre a estrutura de recorrência de tarefa que a função cria, confira a `BuildWeeklyTaskRecurrencePattern` [Propriedade canônica PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md) e a [Propriedade canônica PidLidRecurrencePattern](pidlidrecurrencepattern-canonical-property.md). 

Observe que, embora uma grande variedade de padrões de recorrência seja `BuildWeeklyTaskRecurrencePattern` possível, a função apenas cria um padrão de recorrência semanal. Também é codificado por várias suposições, como o tipo de calendário (gregoriano), o primeiro dia da semana (domingo) e o número de instâncias modificadas ou excluídas (nenhuma). Uma função de criação de padrão de recorrência de finalização mais geral precisaria aceitar esses tipos de variáveis como parâmetros. 
  
Veja a seguir a listagem completa da `AddTask` função. 
  
```cpp
HRESULT AddTask(LPMAPIFOLDER lpFolder,
            SYSTEMTIME* lpstStart, // PidLidCommonEnd, PidLidTaskDueDate, PidLidTaskRecurrence
            SYSTEMTIME* lpstEnd, // PidLidTaskRecurrence
            SYSTEMTIME* lpstFirstDOW, // PidLidTaskRecurrence
            DWORD dwPeriod, // PidLidTaskRecurrence
            DWORD dwOccurrenceCount, // PidLidTaskRecurrence
            DWORD dwPatternTypeSpecific, // PidLidTaskRecurrence
            LPWSTR szSubject, // PR_SUBJECT_W
            LPWSTR szBody) // PR_BODY_W
{
   if (!lpFolder) return MAPI_E_INVALID_PARAMETER;
   HRESULT hRes = S_OK;
   LPMESSAGE lpMessage = 0;
   // create a message and set its properties
   hRes = lpFolder->CreateMessage(0,
      0,
      &lpMessage);
   if (SUCCEEDED(hRes))
   {
      MAPINAMEID  rgnmid[ulTaskProps];
      LPMAPINAMEID rgpnmid[ulTaskProps];
      LPSPropTagArray lpNamedPropTags = NULL;
      ULONG i = 0;
      for (i = 0 ; i < ulTaskProps ; i++)
      {
         if (i < ulFirstTaskProp)
            rgnmid[i].lpguid = (LPGUID)&PSETID_Common;
         else
            rgnmid[i].lpguid = (LPGUID)&PSETID_Task;
         rgnmid[i].ulKind = MNID_ID;
         rgnmid[i].Kind.lID = aulTaskProps[i];
         rgpnmid[i] = &rgnmid[i];
      }
      hRes = lpFolder->GetIDsFromNames(
         ulTaskProps,
         (LPMAPINAMEID*) &rgpnmid,
         NULL,
         &lpNamedPropTags);
      if (SUCCEEDED(hRes) && lpNamedPropTags)
      {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
         SPropValue spvProps[NUM_PROPS] = {0};
         spvProps[p_PidLidTaskMode].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskMode],PT_LONG);
         spvProps[p_PidLidCommonEnd].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCommonEnd],PT_SYSTIME);
         spvProps[p_PidLidTaskStatus].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskStatus],PT_LONG);
         spvProps[p_PidLidPercentComplete].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidPercentComplete],PT_DOUBLE);
         spvProps[p_PidLidTaskState].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskState],PT_LONG);
         spvProps[p_PidLidTaskRecurrence].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskRecurrence],PT_BINARY);
         spvProps[p_PidLidTaskDeadOccurrence].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskDeadOccurrence],PT_BOOLEAN);
         spvProps[p_PidLidTaskOwner].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskOwner],PT_UNICODE);
         spvProps[p_PidLidTaskFRecurring].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskFRecurring],PT_BOOLEAN);
         spvProps[p_PidLidTaskOwnership].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskOwnership],PT_LONG);
         spvProps[p_PidLidTaskAcceptanceState].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskAcceptanceState],PT_LONG);
         spvProps[p_PidLidTaskFFixOffline].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskFFixOffline],PT_BOOLEAN);
         spvProps[p_PidLidTaskDueDate].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskDueDate],PT_SYSTIME);
         spvProps[p_PidLidTaskComplete].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskComplete],PT_SYSTIME);
         spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag   = PR_MESSAGE_CLASS_W;
         spvProps[p_PR_ICON_INDEX].ulPropTag        = PR_ICON_INDEX;
         spvProps[p_PR_SUBJECT_W].ulPropTag         = PR_SUBJECT_W;
         spvProps[p_PR_MESSAGE_FLAGS].ulPropTag     = PR_MESSAGE_FLAGS;
         spvProps[p_PR_BODY_W].ulPropTag            = PR_BODY_W;
         spvProps[p_PidLidTaskMode].Value.l = tdmtNothing;
         SYSTEMTIME stStartUTC = {0};
         TzSpecificLocalTimeToSystemTime(NULL,lpstStart,&stStartUTC);
         SystemTimeToFileTime(&stStartUTC,&spvProps[p_PidLidCommonEnd].Value.ft);
         spvProps[p_PidLidTaskStatus].Value.l = tsvNotStarted;
         spvProps[p_PidLidPercentComplete].Value.dbl = 0.0;
         spvProps[p_PidLidTaskState].Value.l = tdsOWNNEW;
         spvProps[p_PidLidTaskDeadOccurrence].Value.b = false;
         spvProps[p_PidLidTaskOwner].Value.lpszW = L"Unknown";
         spvProps[p_PidLidTaskFRecurring].Value.b = true;
         spvProps[p_PidLidTaskOwnership].Value.l = tovNew;
         spvProps[p_PidLidTaskAcceptanceState].Value.l = tdvNone;
         spvProps[p_PidLidTaskFFixOffline].Value.b = true;
         SystemTimeToFileTime(lpstStart,&spvProps[p_PidLidTaskDueDate].Value.ft);
         spvProps[p_PidLidTaskComplete].Value.b = false;
         spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Task";
         spvProps[p_PR_ICON_INDEX].Value.l = 0x501; // Unassigned Recurring Task
         spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
         spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_READ;
         spvProps[p_PR_BODY_W].Value.lpszW = szBody;
         hRes = BuildWeeklyTaskRecurrencePattern(
            lpstStart,
            lpstEnd,
            lpstFirstDOW,
            dwPeriod,
            dwOccurrenceCount,
            dwPatternTypeSpecific,
            &spvProps[p_PidLidTaskRecurrence].Value.bin.cb,
            &spvProps[p_PidLidTaskRecurrence].Value.bin.lpb);
         if (SUCCEEDED(hRes))
         {
            hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
            if (SUCCEEDED(hRes))
            {
               hRes = lpMessage->SaveChanges(FORCE_SAVE);
            }
         }
         if (spvProps[p_PidLidTaskRecurrence].Value.bin.lpb)
            delete[] spvProps[p_PidLidTaskRecurrence].Value.bin.lpb;
      }
      MAPIFreeBuffer(lpNamedPropTags);
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}

```

## <a name="see-also"></a>Confira também

- [Usando MAPI para criar itens do Outlook 2007](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

