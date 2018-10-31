---
title: Evento FetchProgress (ADO)
TOCTitle: FetchProgress Event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a898ad02d551e0c4de02597761ccd3076fc5eb77
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862273"
---
# <a name="fetchprogress-event-ado"></a><span data-ttu-id="7ee54-102">Evento FetchProgress (ADO)</span><span class="sxs-lookup"><span data-stu-id="7ee54-102">FetchProgress Event (ADO)</span></span>


<span data-ttu-id="7ee54-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ee54-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="7ee54-104">O evento **FetchProgress** é chamado periodicamente durante uma operação assíncrona demorada para relatar quantas linhas adicionais foram recuperadas, no momento, no [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="7ee54-104">The **FetchProgress** event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7ee54-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ee54-105">Syntax</span></span>

<span data-ttu-id="7ee54-106">De*progresso*, *MaxProgress*, de FetchProgress *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="7ee54-106">FetchProgress*Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="7ee54-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ee54-107">Parameters</span></span>

  - <span data-ttu-id="7ee54-108">*Progress*</span><span class="sxs-lookup"><span data-stu-id="7ee54-108">*Progress*</span></span>

  - <span data-ttu-id="7ee54-109">Um valor **Long** que indica o número de registros que foram atualmente recuperados pela operação de busca.</span><span class="sxs-lookup"><span data-stu-id="7ee54-109">A **Long** value indicating the number of records that have currently been retrieved by the fetch operation.</span></span>

  - <span data-ttu-id="7ee54-110">*MaxProgress*</span><span class="sxs-lookup"><span data-stu-id="7ee54-110">*MaxProgress*</span></span>

  - <span data-ttu-id="7ee54-111">Um valor **Long** que indica o número máximo de registros esperados para recuperação.</span><span class="sxs-lookup"><span data-stu-id="7ee54-111">A **Long** value indicating the maximum number of records expected to be retrieved.</span></span>

  - <span data-ttu-id="7ee54-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="7ee54-112">*adStatus*</span></span>

  - <span data-ttu-id="7ee54-113">Um valor de status [EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="7ee54-113">An [EventStatusEnum](eventstatusenum.md) status value.</span></span>

  - <span data-ttu-id="7ee54-114">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="7ee54-114">*pRecordset*</span></span>

  - <span data-ttu-id="7ee54-115">Um objeto **Recordset** que é aquele para o qual os registros estão sendo recuperados.</span><span class="sxs-lookup"><span data-stu-id="7ee54-115">A **Recordset** object that is the object for which the records are being retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ee54-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ee54-116">Remarks</span></span>

<span data-ttu-id="7ee54-117">Ao utilizar o **FetchProgress** com um **Recordset**filho, lembre-se de que os valores de parâmetro de *progresso* e *MaxProgress* são derivados do conjunto de linhas subjacente do [Serviço de Cursor](microsoft-cursor-service-for-ole-db-ado-service-component.md) .</span><span class="sxs-lookup"><span data-stu-id="7ee54-117">When using **FetchProgress** with a child **Recordset**, be aware that the *Progress* and *MaxProgress* parameter values are derived from the underlying [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset.</span></span> <span data-ttu-id="7ee54-118">Os valores retornados representam o número total de registros no conjunto de linhas base, não apenas o número de registros no capítulo atual.</span><span class="sxs-lookup"><span data-stu-id="7ee54-118">The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</span></span>


> [!NOTE]
> <span data-ttu-id="7ee54-119">[!OBSERVAçãO] Para utilizar o **FetchProgress** com o Microsoft Visual Basic, é necessário o Visual Basic 6.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7ee54-119">To use **FetchProgress** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


