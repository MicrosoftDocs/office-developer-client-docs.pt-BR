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
# <a name="about-asynchronous-table-operations"></a><span data-ttu-id="51dc4-103">Sobre operações de tabela assíncronas</span><span class="sxs-lookup"><span data-stu-id="51dc4-103">About asynchronous table operations</span></span>
 
<span data-ttu-id="51dc4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51dc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51dc4-105">A interface **IMAPITable** inclui três métodos que operam de forma assíncrona e três métodos para controlar uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="51dc4-105">The **IMAPITable** interface includes three methods that operate asynchronously and three methods for controlling an asynchronous operation.</span></span> <span data-ttu-id="51dc4-106">A tabela a seguir lista estes métodos:</span><span class="sxs-lookup"><span data-stu-id="51dc4-106">The following table lists these methods:</span></span> 
  
|<span data-ttu-id="51dc4-107">**Operação assíncrona**</span><span class="sxs-lookup"><span data-stu-id="51dc4-107">**Asynchronous operation**</span></span>|<span data-ttu-id="51dc4-108">**Método de controle assíncrono**</span><span class="sxs-lookup"><span data-stu-id="51dc4-108">**Asynchronous control method**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="51dc4-109">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="51dc4-109">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |[<span data-ttu-id="51dc4-110">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="51dc4-110">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md) <br/> |
|[<span data-ttu-id="51dc4-111">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="51dc4-111">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |[<span data-ttu-id="51dc4-112">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="51dc4-112">IMAPITable::Abort</span></span>](imapitable-abort.md) <br/> |
|[<span data-ttu-id="51dc4-113">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="51dc4-113">IMAPITable::SortTable</span></span>](imapitable-sorttable.md) <br/> |[<span data-ttu-id="51dc4-114">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="51dc4-114">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |
   
<span data-ttu-id="51dc4-115">**Para recuperar informações de status sobre o tipo de uma tabela e a operação atual**</span><span class="sxs-lookup"><span data-stu-id="51dc4-115">**To retrieve status information about a table's type and current operation**</span></span>
  
- <span data-ttu-id="51dc4-116">Chame [IMAPITable::GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="51dc4-116">Call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span> <span data-ttu-id="51dc4-117">Com **GetStatus**, um usuário de tabela pode determinar se a tabela é estática ou dinâmica, se uma operação está em andamento ou foi concluída e se ocorreu um erro de uma operação concluída.</span><span class="sxs-lookup"><span data-stu-id="51dc4-117">With **GetStatus**, a table user can determine whether the table is static or dynamic, if an operation is in progress or has completed, and if an error has occurred from a completed operation.</span></span> <span data-ttu-id="51dc4-118">Por exemplo, se um cliente precisar cancelar uma operação de classificação porque está demorando muito, o cliente pode primeiro chamar **GetStatus** para determinar se, na verdade, uma operação de classificação está sendo processada no momento.</span><span class="sxs-lookup"><span data-stu-id="51dc4-118">For example, if a client needs to cancel a sort operation because it is taking too much time, the client can first call **GetStatus** to determine whether, in fact, a sort operation is presently processing.</span></span> <span data-ttu-id="51dc4-119">Em seguida, o cliente pode [chamar IMAPITable::Abort](imapitable-abort.md) para impedi-lo.</span><span class="sxs-lookup"><span data-stu-id="51dc4-119">Then the client can call [IMAPITable::Abort](imapitable-abort.md) to stop it.</span></span> 
    
<span data-ttu-id="51dc4-120">**Para suspender a atividade até que uma tarefa assíncrona seja concluída**</span><span class="sxs-lookup"><span data-stu-id="51dc4-120">**To suspend activity until an asynchronous task has completed**</span></span>
  
- <span data-ttu-id="51dc4-121">Chame [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span><span class="sxs-lookup"><span data-stu-id="51dc4-121">Call [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span></span> <span data-ttu-id="51dc4-122">Chamar **WaitForCompletion** permite que a tarefa seja concluída sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="51dc4-122">Calling **WaitForCompletion** allows the task to complete without interruption.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="51dc4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="51dc4-123">See also</span></span>

- [<span data-ttu-id="51dc4-124">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="51dc4-124">MAPI Tables</span></span>](mapi-tables.md)

