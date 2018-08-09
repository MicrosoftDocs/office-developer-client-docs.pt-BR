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
# <a name="about-asynchronous-table-operations"></a><span data-ttu-id="0096c-103">Sobre as operações de tabela assíncrona</span><span class="sxs-lookup"><span data-stu-id="0096c-103">About asynchronous table operations</span></span>
 
<span data-ttu-id="0096c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0096c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0096c-105">A interface de **IMAPITable** inclui três métodos que operam de forma assíncrona e três métodos para controlar uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="0096c-105">The **IMAPITable** interface includes three methods that operate asynchronously and three methods for controlling an asynchronous operation.</span></span> <span data-ttu-id="0096c-106">A tabela a seguir lista esses métodos:</span><span class="sxs-lookup"><span data-stu-id="0096c-106">The following table lists these methods:</span></span> 
  
|<span data-ttu-id="0096c-107">**Operação assíncrona**</span><span class="sxs-lookup"><span data-stu-id="0096c-107">**Asynchronous operation**</span></span>|<span data-ttu-id="0096c-108">**Método de controle assíncrono**</span><span class="sxs-lookup"><span data-stu-id="0096c-108">**Asynchronous control method**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0096c-109">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="0096c-109">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |[<span data-ttu-id="0096c-110">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="0096c-110">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md) <br/> |
|[<span data-ttu-id="0096c-111">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="0096c-111">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |[<span data-ttu-id="0096c-112">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="0096c-112">IMAPITable::Abort</span></span>](imapitable-abort.md) <br/> |
|[<span data-ttu-id="0096c-113">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="0096c-113">IMAPITable::SortTable</span></span>](imapitable-sorttable.md) <br/> |[<span data-ttu-id="0096c-114">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="0096c-114">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |
   
<span data-ttu-id="0096c-115">**Para recuperar informações de status sobre o tipo e a operação atual de uma tabela**</span><span class="sxs-lookup"><span data-stu-id="0096c-115">**To retrieve status information about a table's type and current operation**</span></span>
  
- <span data-ttu-id="0096c-116">Chame [IMAPITable::GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="0096c-116">Call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span> <span data-ttu-id="0096c-117">Com **GetStatus**, um usuário de tabela pode determinar se a tabela é estático ou dinâmico, se uma operação está em andamento ou foi concluída e se ocorreu um erro de uma operação concluída.</span><span class="sxs-lookup"><span data-stu-id="0096c-117">With **GetStatus**, a table user can determine whether the table is static or dynamic, if an operation is in progress or has completed, and if an error has occurred from a completed operation.</span></span> <span data-ttu-id="0096c-118">Por exemplo, se um cliente precisar cancelar uma operação de classificação, porque ele está demorando muito tempo, o cliente pode chamar primeiro **GetStatus** para determinar se, na verdade, uma operação de classificação está atualmente processando.</span><span class="sxs-lookup"><span data-stu-id="0096c-118">For example, if a client needs to cancel a sort operation because it is taking too much time, the client can first call **GetStatus** to determine whether, in fact, a sort operation is presently processing.</span></span> <span data-ttu-id="0096c-119">Em seguida, o cliente pode chamar [IMAPITable::Abort](imapitable-abort.md) para interrompê-lo.</span><span class="sxs-lookup"><span data-stu-id="0096c-119">Then the client can call [IMAPITable::Abort](imapitable-abort.md) to stop it.</span></span> 
    
<span data-ttu-id="0096c-120">**Para suspender atividade até que uma tarefa assíncrona seja concluída**</span><span class="sxs-lookup"><span data-stu-id="0096c-120">**To suspend activity until an asynchronous task has completed**</span></span>
  
- <span data-ttu-id="0096c-121">Chame [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span><span class="sxs-lookup"><span data-stu-id="0096c-121">Call [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span></span> <span data-ttu-id="0096c-122">Chamar **WaitForCompletion** permite que a tarefa seja concluída sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="0096c-122">Calling **WaitForCompletion** allows the task to complete without interruption.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0096c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0096c-123">See also</span></span>

- [<span data-ttu-id="0096c-124">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="0096c-124">MAPI Tables</span></span>](mapi-tables.md)

