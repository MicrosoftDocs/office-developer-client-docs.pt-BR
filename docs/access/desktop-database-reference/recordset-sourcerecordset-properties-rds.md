---
title: Propriedades Recordset, SourceRecordset (RDS)
TOCTitle: Recordset, SourceRecordset properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f842ad1498e0f6752299cd3d16d8c558042a850e
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945779"
---
# <a name="recordset-sourcerecordset-properties-rds"></a><span data-ttu-id="87090-102">Propriedades Recordset, SourceRecordset (RDS)</span><span class="sxs-lookup"><span data-stu-id="87090-102">Recordset, SourceRecordset properties (RDS)</span></span>


<span data-ttu-id="87090-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="87090-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="87090-104">Indica o objeto **Recordset** retornado de um objeto corporativo personalizado.</span><span class="sxs-lookup"><span data-stu-id="87090-104">Indicates the **Recordset** object returned from a custom business object.</span></span>

## <a name="syntax"></a><span data-ttu-id="87090-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87090-105">Syntax</span></span>

<span data-ttu-id="87090-106">*DataControl*. SourceRecordset = *Recordset*</span><span class="sxs-lookup"><span data-stu-id="87090-106">*DataControl*.SourceRecordset = *Recordset*</span></span>

<span data-ttu-id="87090-107">*Recordset* = *DataControl*. Conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="87090-107">*Recordset* = *DataControl*.Recordset</span></span>

## <a name="parameters"></a><span data-ttu-id="87090-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87090-108">Parameters</span></span>

- <span data-ttu-id="87090-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="87090-109">*DataControl*</span></span>

  - <span data-ttu-id="87090-110">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="87090-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

- <span data-ttu-id="87090-111">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="87090-111">*Recordset*</span></span>

  - <span data-ttu-id="87090-112">Uma variável de objeto que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="87090-112">An object variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="87090-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="87090-113">Remarks</span></span>

<span data-ttu-id="87090-114">Você pode definir a propriedade **SourceRecordset** para um [Recordset](recordset-object-ado.md) retornado por um objeto comercial personalizado.</span><span class="sxs-lookup"><span data-stu-id="87090-114">You can set the **SourceRecordset** property to a [Recordset](recordset-object-ado.md) returned from a custom business object.</span></span>

<span data-ttu-id="87090-p101">Essas propriedades permitem que um aplicativo trate do processo de ligação por um processo personalizado. Elas recebem um conjunto de linhas disposto em um **Recordset**, de forma que você possa interagir diretamente com o **Recordset**, executando ações como a definição de propriedades ou interagindo por meio do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="87090-p101">These properties allow an application to handle the binding process by means of a custom process. They receive a rowset wrapped in a **Recordset** so that you can interact directly with the **Recordset**, performing actions such as setting properties or iterating through the **Recordset**.</span></span>

<span data-ttu-id="87090-117">Você pode definir a propriedade **SourceRecordset** ou ler a propriedade **Recordset** em tempo de execução no código de script.</span><span class="sxs-lookup"><span data-stu-id="87090-117">You can set the **SourceRecordset** property or read the **Recordset** property at run time in scripting code.</span></span>

<span data-ttu-id="87090-118">**SourceRecordset** é uma propriedade somente gravação, ao contrário da propriedade **Recordset**, que é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="87090-118">**SourceRecordset** is a write-only property, in contrast to the **Recordset** property, which is a read-only property.</span></span>

