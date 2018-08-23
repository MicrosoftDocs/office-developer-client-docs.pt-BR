---
title: Criar um item de tarefa recorrente simples
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e9ee8865-0983-439e-8405-7946c5ec8762
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 68d7472f993bcc35abbd4b733bae9f137b948608
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576838"
---
# <a name="create-a-simple-recurrent-task-item"></a>Criar um item de tarefa recorrente simples

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI pode ser usado para criar para criar itens de tarefa. Este tópico descreve como criar um item de tarefa recorrente simples.
  
Para obter informações sobre como baixar, ler e executar o código do aplicativo MFCMAPI e projeto CreateOutlookItemsAddin referenciado neste tópico, consulte [instalar amostras usadas na seção deste](how-to-install-the-samples-used-in-this-section.md).

### <a name="to-create-a-task-item"></a>Para criar um item de tarefa

1. Abra um armazenamento de mensagens. Para obter informações sobre como abrir um armazenamento de mensagens, consulte [Abrindo um armazenamento de mensagens](opening-a-message-store.md).
    
2. Abra a pasta de tarefas no repositório de mensagem. Para obter mais informações, consulte **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).
    
3. Chame o método de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) na pasta de tarefas para criar o novo item de tarefa. 
    
4. Defina a propriedade **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) e outras propriedades relacionados a tarefas necessárias para criar uma tarefa recorrente.
    
5. Salve o novo item de tarefa.
    
O `AddTask` função no arquivo de origem Tasks.cpp do projeto CreateOutlookItemsAddin demonstra estas etapas. O `AddTask` função usa os parâmetros da caixa de diálogo **Adicionar tarefa** é exibida quando você clicar em **Adicionar tarefa** no menu **Addins** no aplicativo de amostra MFCMAPI. O `DisplayAddTaskDialog` funcione no Tasks.cpp exibe a caixa de diálogo e passa os valores da caixa de diálogo para o `AddTask` função. O `DisplayAddTaskDialog` função não se relacionam diretamente para a criação de um item de tarefa usando MAPI, portanto, não está listado aqui. 
  
> [!IMPORTANT]
> O código no aplicativo MFCMAPI não garante que a pasta **tarefas** foi selecionada quando você clicar no comando **Adicionar tarefa** no menu **Addins** . Criando itens de tarefa em uma pasta diferente da pasta **tarefas** pode causar um comportamento indefinido. Certifique-se de que você selecionou a pasta de **tarefas** antes de usar o comando **Adicionar tarefa** no aplicativo MFCMAPI. 
  
O `AddTask` função está listada abaixo. Observe que o parâmetro _lpFolder_ passado para o `AddTask` função é um ponteiro para uma interface [IMAPIFolder](imapifolderimapicontainer.md) que representa a pasta onde a nova tarefa é criada. Dado o _lpFolder_ que representa uma interface **IMAPIFolder** , o código chama o método de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . O método **CreateMessage** retorna um código de sucesso e um ponteiro para um ponteiro para uma interface **IMessage** . A maioria do `AddTask` o trabalho de especificação de propriedades em preparação para chamar o método [IMAPIProp::SetProps](imapiprop-setprops.md) lida com o código de função. Se a chamada para o método **SetProps** tiver êxito, o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) é chamado para confirmar as alterações para o repositório e criar um novo item de tarefa. 
  
O `AddTask` função define um número de propriedades nomeadas. Para obter informações sobre propriedades nomeadas e como eles são criados, consulte [Usando MAPI para criar itens do Outlook 2007](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx). Porque as propriedades nomeadas usadas para itens de tarefa ocupam vários conjuntos de propriedade, deve ter cuidado ao construir parâmetros a serem passados para o método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . 
  
O `AddTask` funcionar usa o `BuildWeeklyTaskRecurrencePattern` função auxiliar para criar uma estrutura que representa uma tarefa recorrente para a configuração da propriedade **dispidTaskRecur** . Para obter informações sobre a estrutura de recorrência da tarefa a `BuildWeeklyTaskRecurrencePattern` function compilações, consulte [Propriedades de canônico PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md) e [PidLidRecurrencePattern canônico](pidlidrecurrencepattern-canonical-property.md). 

Observe que, enquanto uma grande variedade de padrões de recorrência, são possíveis, o `BuildWeeklyTaskRecurrencePattern` função apenas cria um padrão de recorrência semanal. Também é difícil codificados para um número de suposições, como o tipo de calendário (Gregoriano), o primeiro dia da semana (domingo) e o número de instâncias modificados ou excluídos (nenhum). Uma finalidade mais geral função de criação de padrão de recorrência precisaria aceitar esses tipos de variáveis como parâmetros. 
  
O seguinte é a lista completa do `AddTask` função. 
  
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

- [Usando MAPI para criar itens do Outlook 2007](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

