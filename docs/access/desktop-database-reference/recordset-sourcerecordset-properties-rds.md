---
title: Propriedades Recordset, SourceRecordset (RDS)
TOCTitle: Recordset, SourceRecordset properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f83ab385b1fab511ab71ea9ff3456fe466efa17c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703521"
---
# <a name="recordset-sourcerecordset-properties-rds"></a><span data-ttu-id="fcfb4-102">Propriedades Recordset, SourceRecordset (RDS)</span><span class="sxs-lookup"><span data-stu-id="fcfb4-102">Recordset, SourceRecordset properties (RDS)</span></span>

<span data-ttu-id="fcfb4-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="fcfb4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fcfb4-104">Indica o objeto **Recordset** retornado de um objeto corporativo personalizado.</span><span class="sxs-lookup"><span data-stu-id="fcfb4-104">Indicates the **Recordset** object returned from a custom business object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcfb4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcfb4-105">Syntax</span></span>

<span data-ttu-id="fcfb4-106">*DataControl*. SourceRecordset = *Recordset*</span><span class="sxs-lookup"><span data-stu-id="fcfb4-106">*DataControl*.SourceRecordset = *Recordset*</span></span>

<span data-ttu-id="fcfb4-107">*Recordset* = *DataControl*. Conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="fcfb4-107">*Recordset* = *DataControl*.Recordset</span></span>

## <a name="parameters"></a><span data-ttu-id="fcfb4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcfb4-108">Parameters</span></span>

|<span data-ttu-id="fcfb4-109">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="fcfb4-109">Parameter</span></span>|<span data-ttu-id="fcfb4-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="fcfb4-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="fcfb4-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="fcfb4-111">*DataControl*</span></span> |<span data-ttu-id="fcfb4-112">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="fcfb4-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="fcfb4-113">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="fcfb4-113">*Recordset*</span></span> |<span data-ttu-id="fcfb4-114">Uma variável de objeto que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="fcfb4-114">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="fcfb4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcfb4-115">Remarks</span></span>

<span data-ttu-id="fcfb4-116">Você pode definir a propriedade **SourceRecordset** para um [Recordset](recordset-object-ado.md) retornado por um objeto comercial personalizado.</span><span class="sxs-lookup"><span data-stu-id="fcfb4-116">You can set the **SourceRecordset** property to a [Recordset](recordset-object-ado.md) returned from a custom business object.</span></span>

<span data-ttu-id="fcfb4-p101">Essas propriedades permitem que um aplicativo trate do processo de ligação por um processo personalizado. Elas recebem um conjunto de linhas disposto em um **Recordset**, de forma que você possa interagir diretamente com o **Recordset**, executando ações como a definição de propriedades ou interagindo por meio do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="fcfb4-p101">These properties allow an application to handle the binding process by means of a custom process. They receive a rowset wrapped in a **Recordset** so that you can interact directly with the **Recordset**, performing actions such as setting properties or iterating through the **Recordset**.</span></span>

<span data-ttu-id="fcfb4-119">Você pode definir a propriedade **SourceRecordset** ou ler a propriedade **Recordset** em tempo de execução no código de script.</span><span class="sxs-lookup"><span data-stu-id="fcfb4-119">You can set the **SourceRecordset** property or read the **Recordset** property at run time in scripting code.</span></span>

<span data-ttu-id="fcfb4-120">**SourceRecordset** é uma propriedade somente gravação, ao contrário da propriedade **Recordset**, que é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fcfb4-120">**SourceRecordset** is a write-only property, in contrast to the **Recordset** property, which is a read-only property.</span></span>

