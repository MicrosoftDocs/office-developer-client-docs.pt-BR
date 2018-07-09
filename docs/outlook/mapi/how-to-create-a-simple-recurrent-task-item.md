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
ms.openlocfilehash: 926b33fa3627461139362737f86248f217191534
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766712"
---
# <a name="create-a-simple-recurrent-task-item"></a><span data-ttu-id="bd2fe-103">Criar um item de tarefa recorrente simples</span><span class="sxs-lookup"><span data-stu-id="bd2fe-103">Create a simple recurrent task item</span></span>

<span data-ttu-id="bd2fe-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd2fe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bd2fe-105">MAPI pode ser usado para criar para criar itens de tarefa.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-105">MAPI can be used to create to create task items.</span></span> <span data-ttu-id="bd2fe-106">Este tópico descreve como criar um item de tarefa recorrente simples.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-106">This topic describes how to create a simple recurrent task item.</span></span>
  
<span data-ttu-id="bd2fe-107">Para obter informações sobre como baixar, ler e executar o código do aplicativo MFCMAPI e projeto CreateOutlookItemsAddin referenciado neste tópico, consulte [instalar amostras usadas na seção deste](how-to-install-the-samples-used-in-this-section.md).</span><span class="sxs-lookup"><span data-stu-id="bd2fe-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-create-a-task-item"></a><span data-ttu-id="bd2fe-108">Para criar um item de tarefa</span><span class="sxs-lookup"><span data-stu-id="bd2fe-108">To create a task item</span></span>

1. <span data-ttu-id="bd2fe-109">Abra um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-109">Open a message store.</span></span> <span data-ttu-id="bd2fe-110">Para obter informações sobre como abrir um armazenamento de mensagens, consulte [Abrindo um armazenamento de mensagens](opening-a-message-store.md).</span><span class="sxs-lookup"><span data-stu-id="bd2fe-110">For information on how to open a message store, see [Opening a Message Store](opening-a-message-store.md).</span></span>
    
2. <span data-ttu-id="bd2fe-111">Abra a pasta de tarefas no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-111">Open the Tasks folder in the message store.</span></span> <span data-ttu-id="bd2fe-112">Para obter mais informações, consulte **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bd2fe-112">For more information, see **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="bd2fe-113">Chame o método de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) na pasta de tarefas para criar o novo item de tarefa.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-113">Call the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method on the Tasks folder to create the new task item.</span></span> 
    
4. <span data-ttu-id="bd2fe-114">Defina a propriedade **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) e outras propriedades relacionados a tarefas necessárias para criar uma tarefa recorrente.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-114">Set the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) property and other task-related properties required to create a recurrent task.</span></span>
    
5. <span data-ttu-id="bd2fe-115">Salve o novo item de tarefa.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-115">Save the new task item.</span></span>
    
<span data-ttu-id="bd2fe-116">O `AddTask` função no arquivo de origem Tasks.cpp do projeto CreateOutlookItemsAddin demonstra estas etapas.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-116">The  `AddTask` function in the Tasks.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="bd2fe-117">O `AddTask` função usa os parâmetros da caixa de diálogo **Adicionar tarefa** é exibida quando você clicar em **Adicionar tarefa** no menu **Addins** no aplicativo de amostra MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-117">The  `AddTask` function takes parameters from the **Add Task** dialog box that is displayed when you click **Add Task** on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="bd2fe-118">O `DisplayAddTaskDialog` funcione no Tasks.cpp exibe a caixa de diálogo e passa os valores da caixa de diálogo para o `AddTask` função.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-118">The  `DisplayAddTaskDialog` function in Tasks.cpp displays the dialog box and passes values from the dialog box to the  `AddTask` function.</span></span> <span data-ttu-id="bd2fe-119">O `DisplayAddTaskDialog` função não se relacionam diretamente para a criação de um item de tarefa usando MAPI, portanto, não está listado aqui.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-119">The  `DisplayAddTaskDialog` function does not relate directly to creating a task item using MAPI, so it is not listed here.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="bd2fe-120">O código no aplicativo MFCMAPI não garante que a pasta **tarefas** foi selecionada quando você clicar no comando **Adicionar tarefa** no menu **Addins** .</span><span class="sxs-lookup"><span data-stu-id="bd2fe-120">The code in the MFCMAPI application does not ensure that the **Tasks** folder has been selected when you click the **Add Task** command on the **Addins** menu.</span></span> <span data-ttu-id="bd2fe-121">Criando itens de tarefa em uma pasta diferente da pasta **tarefas** pode causar um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-121">Creating task items in a folder other than the **Tasks** folder can cause undefined behavior.</span></span> <span data-ttu-id="bd2fe-122">Certifique-se de que você selecionou a pasta de **tarefas** antes de usar o comando **Adicionar tarefa** no aplicativo MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-122">Make sure that you have selected the **Tasks** folder before using the **Add Task** command in the MFCMAPI application.</span></span> 
  
<span data-ttu-id="bd2fe-123">O `AddTask` função está listada abaixo.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-123">The  `AddTask` function is listed below.</span></span> <span data-ttu-id="bd2fe-124">Observe que o parâmetro _lpFolder_ passado para o `AddTask` função é um ponteiro para uma interface [IMAPIFolder](imapifolderimapicontainer.md) que representa a pasta onde a nova tarefa é criada.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-124">Note that the  _lpFolder_ parameter passed to the  `AddTask` function is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new task is created.</span></span> <span data-ttu-id="bd2fe-125">Dado o _lpFolder_ que representa uma interface **IMAPIFolder** , o código chama o método de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="bd2fe-125">Given the  _lpFolder_ that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="bd2fe-126">O método **CreateMessage** retorna um código de sucesso e um ponteiro para um ponteiro para uma interface **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="bd2fe-126">The **CreateMessage** method returns a success code and a pointer to a pointer to an **IMessage** interface.</span></span> <span data-ttu-id="bd2fe-127">A maioria do `AddTask` o trabalho de especificação de propriedades em preparação para chamar o método [IMAPIProp::SetProps](imapiprop-setprops.md) lida com o código de função.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-127">Most of the  `AddTask` function code handles the work of specifying properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="bd2fe-128">Se a chamada para o método **SetProps** tiver êxito, o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) é chamado para confirmar as alterações para o repositório e criar um novo item de tarefa.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-128">If the call to the **SetProps** method succeeds, the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called to commit the changes to the store and create a new task item.</span></span> 
  
<span data-ttu-id="bd2fe-129">O `AddTask` função define um número de propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-129">The  `AddTask` function sets a number of named properties.</span></span> <span data-ttu-id="bd2fe-130">Para obter informações sobre propriedades nomeadas e como eles são criados, consulte [Usando MAPI para criar itens do Outlook 2007](http://msdn.microsoft.com/pt-br/library/cc678348%28office.12%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="bd2fe-130">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](http://msdn.microsoft.com/pt-br/library/cc678348%28office.12%29.aspx).</span></span> <span data-ttu-id="bd2fe-131">Porque as propriedades nomeadas usadas para itens de tarefa ocupam vários conjuntos de propriedade, deve ter cuidado ao construir parâmetros a serem passados para o método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="bd2fe-131">Because the named properties used for task items occupy multiple property sets, care must be taken when building parameters to pass to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="bd2fe-132">O `AddTask` funcionar usa o `BuildWeeklyTaskRecurrencePattern` função auxiliar para criar uma estrutura que representa uma tarefa recorrente para a configuração da propriedade **dispidTaskRecur** .</span><span class="sxs-lookup"><span data-stu-id="bd2fe-132">The  `AddTask` function uses the  `BuildWeeklyTaskRecurrencePattern` helper function to build a structure representing a task recurrence for setting the **dispidTaskRecur** property.</span></span> <span data-ttu-id="bd2fe-133">Para obter informações sobre a estrutura de recorrência da tarefa a `BuildWeeklyTaskRecurrencePattern` function compilações, consulte [Propriedades de canônico PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md) e [PidLidRecurrencePattern canônico](pidlidrecurrencepattern-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="bd2fe-133">For information on the task recurrence structure the  `BuildWeeklyTaskRecurrencePattern` function builds, see [PidLidTaskRecurrence Canonical Property](pidlidtaskrecurrence-canonical-property.md) and [PidLidRecurrencePattern Canonical Property](pidlidrecurrencepattern-canonical-property.md).</span></span> 

<span data-ttu-id="bd2fe-134">Observe que, enquanto uma grande variedade de padrões de recorrência, são possíveis, o `BuildWeeklyTaskRecurrencePattern` função apenas cria um padrão de recorrência semanal.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-134">Note that while a large variety of recurrence patterns are possible, the  `BuildWeeklyTaskRecurrencePattern` function only builds a weekly recurrence pattern.</span></span> <span data-ttu-id="bd2fe-135">Também é difícil codificados para um número de suposições, como o tipo de calendário (Gregoriano), o primeiro dia da semana (domingo) e o número de instâncias modificados ou excluídos (nenhum).</span><span class="sxs-lookup"><span data-stu-id="bd2fe-135">It is also hard coded for a number of assumptions, such as the calendar type (Gregorian), the first day of the week (Sunday), and the number of modified or deleted instances (none).</span></span> <span data-ttu-id="bd2fe-136">Uma finalidade mais geral função de criação de padrão de recorrência precisaria aceitar esses tipos de variáveis como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-136">A more general purpose recurrence pattern creation function would need to accept these sorts of variables as parameters.</span></span> 
  
<span data-ttu-id="bd2fe-137">O seguinte é a lista completa do `AddTask` função.</span><span class="sxs-lookup"><span data-stu-id="bd2fe-137">The following is the complete listing of the  `AddTask` function.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="bd2fe-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd2fe-138">See also</span></span>

- [<span data-ttu-id="bd2fe-139">Usando MAPI para criar itens do Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="bd2fe-139">Using MAPI to Create Outlook 2007 Items</span></span>](http://msdn.microsoft.com/pt-br/library/cc678348%28office.12%29.aspx)

