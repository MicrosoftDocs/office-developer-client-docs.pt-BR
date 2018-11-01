---
title: Evento FetchProgress (ADO)
TOCTitle: FetchProgress Event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25d062f4ae7008df787394eeb9253b65d6f5d1c8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886190"
---
# <a name="fetchprogress-event-ado"></a><span data-ttu-id="bc2a1-102">Evento FetchProgress (ADO)</span><span class="sxs-lookup"><span data-stu-id="bc2a1-102">FetchProgress Event (ADO)</span></span>


<span data-ttu-id="bc2a1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc2a1-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="bc2a1-104">O evento **FetchProgress** é chamado periodicamente durante uma operação assíncrona demorada para relatar quantas linhas adicionais foram recuperadas, no momento, no [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="bc2a1-104">The **FetchProgress** event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc2a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc2a1-105">Syntax</span></span>

<span data-ttu-id="bc2a1-106">De*progresso*, *MaxProgress*, de FetchProgress *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="bc2a1-106">FetchProgress*Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="bc2a1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc2a1-107">Parameters</span></span>

  - <span data-ttu-id="bc2a1-108">*Progress*</span><span class="sxs-lookup"><span data-stu-id="bc2a1-108">*Progress*</span></span>

  - <span data-ttu-id="bc2a1-109">Um valor **Long** que indica o número de registros que foram atualmente recuperados pela operação de busca.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-109">A **Long** value indicating the number of records that have currently been retrieved by the fetch operation.</span></span>

  - <span data-ttu-id="bc2a1-110">*MaxProgress*</span><span class="sxs-lookup"><span data-stu-id="bc2a1-110">*MaxProgress*</span></span>

  - <span data-ttu-id="bc2a1-111">Um valor **Long** que indica o número máximo de registros esperados para recuperação.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-111">A **Long** value indicating the maximum number of records expected to be retrieved.</span></span>

  - <span data-ttu-id="bc2a1-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="bc2a1-112">*adStatus*</span></span>

  - <span data-ttu-id="bc2a1-113">Um valor de status [EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="bc2a1-113">An [EventStatusEnum](eventstatusenum.md) status value.</span></span>

  - <span data-ttu-id="bc2a1-114">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="bc2a1-114">*pRecordset*</span></span>

  - <span data-ttu-id="bc2a1-115">Um objeto **Recordset** que é aquele para o qual os registros estão sendo recuperados.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-115">A **Recordset** object that is the object for which the records are being retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc2a1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc2a1-116">Remarks</span></span>

<span data-ttu-id="bc2a1-117">Ao utilizar o **FetchProgress** com um **Recordset**filho, lembre-se de que os valores de parâmetro de *progresso* e *MaxProgress* são derivados do conjunto de linhas subjacente do [Serviço de Cursor](microsoft-cursor-service-for-ole-db-ado-service-component.md) .</span><span class="sxs-lookup"><span data-stu-id="bc2a1-117">When using **FetchProgress** with a child **Recordset**, be aware that the *Progress* and *MaxProgress* parameter values are derived from the underlying [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset.</span></span> <span data-ttu-id="bc2a1-118">Os valores retornados representam o número total de registros no conjunto de linhas base, não apenas o número de registros no capítulo atual.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-118">The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</span></span>


> [!NOTE]
> <span data-ttu-id="bc2a1-119">[!OBSERVAçãO] Para utilizar o **FetchProgress** com o Microsoft Visual Basic, é necessário o Visual Basic 6.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-119">To use **FetchProgress** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


