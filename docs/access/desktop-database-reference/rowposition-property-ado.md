---
title: Propriedade RowPosition (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84d3ad7cc5b3d43b15ac1113f6fa00932678ebc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306857"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="6c383-102">Propriedade RowPosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="6c383-102">RowPosition property (ADO)</span></span>

<span data-ttu-id="6c383-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c383-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6c383-104">Obtém ou define um objeto **RowPosition** do OLE DB a partir de/em um objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="6c383-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="6c383-105">Quando você usa **colocar \_ RowPosition** para definir o objeto **RowPosition,** o objeto **Recordset** resultante usa o objeto **RowPosition** para determinar a linha atual.</span><span class="sxs-lookup"><span data-stu-id="6c383-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="6c383-106">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6c383-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c383-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c383-107">Syntax</span></span>

<span data-ttu-id="6c383-108">HRESULT get \_ RowPosition( \[ out, retval \] IUnknown \* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="6c383-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="6c383-109">HRESULT put \_ RowPosition( \[ in \] IUnknown \* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="6c383-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="6c383-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c383-110">Parameters</span></span>

|<span data-ttu-id="6c383-111">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c383-111">Parameter</span></span>|<span data-ttu-id="6c383-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c383-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="6c383-113">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="6c383-113">*ppRowPos*</span></span> |<span data-ttu-id="6c383-114">Ponteiro para um objeto **RowPosition** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="6c383-114">Pointer to an OLE DB **RowPosition** object.</span></span>|
|<span data-ttu-id="6c383-115">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="6c383-115">*PRowPos*</span></span> |<span data-ttu-id="6c383-116">Um objeto **RowPosition** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="6c383-116">An OLE DB **RowPosition** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="6c383-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6c383-117">Return values</span></span>

<span data-ttu-id="6c383-118">Esse método de propriedade retorna os valores HRESULT padrão, incluindo S \_ OK e E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="6c383-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c383-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c383-119">Remarks</span></span>

<span data-ttu-id="6c383-p102">Quando esta propriedade for definida, se o objeto  **Rowset** no objeto **RowPosition** for diferente do objeto **Rowset** no objeto **Recordset**, o primeiro substituirá o segundo. O mesmo comportamento também se aplicará ao **Charter** atual do **RowPosition**.</span><span class="sxs-lookup"><span data-stu-id="6c383-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="6c383-122">Aplicável a</span><span class="sxs-lookup"><span data-stu-id="6c383-122">Applies to</span></span>

[<span data-ttu-id="6c383-123">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="6c383-123">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

