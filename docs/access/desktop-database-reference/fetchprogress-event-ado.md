---
title: Evento FetchProgress (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d863f51e7836acdc577ecd720df77114ed66f067
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293179"
---
# <a name="fetchprogress-event-ado"></a><span data-ttu-id="6354f-102">Evento FetchProgress (ADO)</span><span class="sxs-lookup"><span data-stu-id="6354f-102">FetchProgress event (ADO)</span></span>

<span data-ttu-id="6354f-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6354f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6354f-104">O evento **FetchProgress** é chamado periodicamente durante uma operação assíncrona demorada para relatar quantas linhas adicionais foram recuperadas, no momento, no [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6354f-104">The **FetchProgress** event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6354f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6354f-105">Syntax</span></span>

<span data-ttu-id="6354f-106">FetchProgress*Progress*, *MaxProgress*, *adStatus*, \*\* precaboset</span><span class="sxs-lookup"><span data-stu-id="6354f-106">FetchProgress*Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="6354f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6354f-107">Parameters</span></span>

|<span data-ttu-id="6354f-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="6354f-108">Parameter</span></span>|<span data-ttu-id="6354f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6354f-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="6354f-110">*Progress*</span><span class="sxs-lookup"><span data-stu-id="6354f-110">*Progress*</span></span> |<span data-ttu-id="6354f-111">Um valor **Long** que indica o número de registros que foram atualmente recuperados pela operação de busca.</span><span class="sxs-lookup"><span data-stu-id="6354f-111">A **Long** value indicating the number of records that have currently been retrieved by the fetch operation.</span></span>|
|<span data-ttu-id="6354f-112">*MaxProgress*</span><span class="sxs-lookup"><span data-stu-id="6354f-112">*MaxProgress*</span></span> |<span data-ttu-id="6354f-113">Um valor **Long** que indica o número máximo de registros esperados para recuperação.</span><span class="sxs-lookup"><span data-stu-id="6354f-113">A **Long** value indicating the maximum number of records expected to be retrieved.</span></span>|
|<span data-ttu-id="6354f-114">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="6354f-114">*adStatus*</span></span> |<span data-ttu-id="6354f-115">Um valor de status [EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="6354f-115">An [EventStatusEnum](eventstatusenum.md) status value.</span></span>|
|<span data-ttu-id="6354f-116">*precaboset*</span><span class="sxs-lookup"><span data-stu-id="6354f-116">*pRecordset*</span></span> |<span data-ttu-id="6354f-117">Um objeto **Recordset** que é aquele para o qual os registros estão sendo recuperados.</span><span class="sxs-lookup"><span data-stu-id="6354f-117">A **Recordset** object that is the object for which the records are being retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="6354f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="6354f-118">Remarks</span></span>

<span data-ttu-id="6354f-p101">Ao utilizar o **FetchProgress** com um **Recordset** filho, esteja ciente de que os valores de parâmetro *Progress* e *MaxProgress* são derivados do [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset base. Os valores retornados representam o número total de registros no conjunto de linhas base, não apenas o número de registros no capítulo atual.</span><span class="sxs-lookup"><span data-stu-id="6354f-p101">When using **FetchProgress** with a child **Recordset**, be aware that the *Progress* and *MaxProgress* parameter values are derived from the underlying [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset. The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="6354f-121">[!OBSERVAçãO] Para utilizar o **FetchProgress** com o Microsoft Visual Basic, é necessário o Visual Basic 6.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6354f-121">To use **FetchProgress** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


