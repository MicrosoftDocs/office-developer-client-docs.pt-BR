---
title: Propriedade RowPosition (ADO)
TOCTitle: RowPosition Property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a4512157e70f4f5a7533e2a480dd96aa3693741
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462843"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="6d6c5-102">Propriedade RowPosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="6d6c5-102">RowPosition Property (ADO)</span></span>


<span data-ttu-id="6d6c5-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d6c5-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="6d6c5-104">Obtém ou define um objeto **RowPosition** do OLE DB a partir de/em um objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="6d6c5-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="6d6c5-105">Quando você usa **colocar\_RowPosition** para definir o objeto **RowPosition** , o objeto **Recordset** resultante usa o objeto **RowPosition** para determinar a linha atual.</span><span class="sxs-lookup"><span data-stu-id="6d6c5-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="6d6c5-106">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6d6c5-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d6c5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d6c5-107">Syntax</span></span>

<span data-ttu-id="6d6c5-108">Get HRESULT\_RowPosition (\[check-out, retval\] IUnknown\* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="6d6c5-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="6d6c5-109">Colocar HRESULT\_RowPosition (\[na\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="6d6c5-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="6d6c5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d6c5-110">Parameters</span></span>

  - <span data-ttu-id="6d6c5-111">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="6d6c5-111">*ppRowPos*</span></span>

  - <span data-ttu-id="6d6c5-112">Ponteiro para um objeto **RowPosition** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="6d6c5-112">Pointer to an OLE DB **RowPosition** object.</span></span>

  - <span data-ttu-id="6d6c5-113">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="6d6c5-113">*PRowPos*</span></span>

  - <span data-ttu-id="6d6c5-114">Um objeto **RowPosition** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="6d6c5-114">An OLE DB **RowPosition** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="6d6c5-115">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="6d6c5-115">Return Values</span></span>

<span data-ttu-id="6d6c5-116">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="6d6c5-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d6c5-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d6c5-117">Remarks</span></span>

<span data-ttu-id="6d6c5-p102">Quando esta propriedade for definida, se o objeto **Rowset** no objeto **RowPosition** for diferente do objeto **Rowset** no objeto **Recordset**, o primeiro substituirá o segundo. O mesmo comportamento também se aplicará ao **Charter** atual do **RowPosition**.</span><span class="sxs-lookup"><span data-stu-id="6d6c5-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="6d6c5-120">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="6d6c5-120">Applies To</span></span>

[<span data-ttu-id="6d6c5-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="6d6c5-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

