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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329012"
---
# <a name="about-asynchronous-table-operations"></a><span data-ttu-id="fce6c-103">Sobre operações de tabela assíncronas</span><span class="sxs-lookup"><span data-stu-id="fce6c-103">About asynchronous table operations</span></span>
 
<span data-ttu-id="fce6c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fce6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fce6c-105">A \*\*\*\* interface IMAPITable inclui três métodos que operam de forma assíncrona e três métodos para controlar uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="fce6c-105">The **IMAPITable** interface includes three methods that operate asynchronously and three methods for controlling an asynchronous operation.</span></span> <span data-ttu-id="fce6c-106">A tabela a seguir lista esses métodos:</span><span class="sxs-lookup"><span data-stu-id="fce6c-106">The following table lists these methods:</span></span> 
  
|<span data-ttu-id="fce6c-107">**Operação asSíncrona**</span><span class="sxs-lookup"><span data-stu-id="fce6c-107">**Asynchronous operation**</span></span>|<span data-ttu-id="fce6c-108">**Método de controle assíncrono**</span><span class="sxs-lookup"><span data-stu-id="fce6c-108">**Asynchronous control method**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fce6c-109">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="fce6c-109">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |[<span data-ttu-id="fce6c-110">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="fce6c-110">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md) <br/> |
|[<span data-ttu-id="fce6c-111">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="fce6c-111">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |[<span data-ttu-id="fce6c-112">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="fce6c-112">IMAPITable::Abort</span></span>](imapitable-abort.md) <br/> |
|[<span data-ttu-id="fce6c-113">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="fce6c-113">IMAPITable::SortTable</span></span>](imapitable-sorttable.md) <br/> |[<span data-ttu-id="fce6c-114">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="fce6c-114">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |
   
<span data-ttu-id="fce6c-115">**Para recuperar as informações de status sobre o tipo de tabela e a operação atual**</span><span class="sxs-lookup"><span data-stu-id="fce6c-115">**To retrieve status information about a table's type and current operation**</span></span>
  
- <span data-ttu-id="fce6c-116">Call [IMAPITable:: GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="fce6c-116">Call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span> <span data-ttu-id="fce6c-117">Com **GetStatus**, um usuário de tabela pode determinar se a tabela é estática ou dinâmica, se uma operação estiver em andamento ou tiver sido concluída e se um erro ocorreu de uma operação concluída.</span><span class="sxs-lookup"><span data-stu-id="fce6c-117">With **GetStatus**, a table user can determine whether the table is static or dynamic, if an operation is in progress or has completed, and if an error has occurred from a completed operation.</span></span> <span data-ttu-id="fce6c-118">Por exemplo, se um cliente precisa cancelar uma operação de classificação porque está demorando muito tempo, o cliente pode primeiro chamar **GetStatus** para determinar se, na verdade, uma operação de classificação está sendo processada no momento.</span><span class="sxs-lookup"><span data-stu-id="fce6c-118">For example, if a client needs to cancel a sort operation because it is taking too much time, the client can first call **GetStatus** to determine whether, in fact, a sort operation is presently processing.</span></span> <span data-ttu-id="fce6c-119">Em seguida, o cliente pode chamar imApitable [:: Abort](imapitable-abort.md) para interrompê-lo.</span><span class="sxs-lookup"><span data-stu-id="fce6c-119">Then the client can call [IMAPITable::Abort](imapitable-abort.md) to stop it.</span></span> 
    
<span data-ttu-id="fce6c-120">**Para suspender a atividade até que uma tarefa assíncrona tenha sido concluída**</span><span class="sxs-lookup"><span data-stu-id="fce6c-120">**To suspend activity until an asynchronous task has completed**</span></span>
  
- <span data-ttu-id="fce6c-121">Call [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md).</span><span class="sxs-lookup"><span data-stu-id="fce6c-121">Call [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span></span> <span data-ttu-id="fce6c-122">Chamar **WaitForCompletion** permite que a tarefa seja concluída sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="fce6c-122">Calling **WaitForCompletion** allows the task to complete without interruption.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="fce6c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fce6c-123">See also</span></span>

- [<span data-ttu-id="fce6c-124">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="fce6c-124">MAPI Tables</span></span>](mapi-tables.md)

